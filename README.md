# LumoJam 🎮

Bem-vindo(a) ao repositório principal do **LumoJam**. 

Para manter o projeto escalável, limpo e livre de conflitos de merge durante o desenvolvimento, estamos adotando uma arquitetura rigorosa de organização e nomenclatura baseada no [UE Style Guide](https://github.com/Allar/ue5-style-guide), mas perfeitamente adaptada para a Unity.

Leia este documento com atenção antes de realizar o seu primeiro commit.

---

## 1. Estrutura de Diretórios e Pastas

Para evitar que o projeto vire um caos, seguimos regras estritas para a criação de pastas:

*   **A Raiz é Sagrada:** Todos os arquivos criados pela nossa equipe devem viver **exclusivamente** dentro da pasta `Assets/LumoJam/`. A raiz de `Assets/` fica reservada apenas para plugins de terceiros e pacotes da engine.
*   **Pastas por Contexto, não por Tipo:** Não crie pastas genéricas como `Texturas/` ou `Scripts/`. Agrupe os arquivos pelo contexto da funcionalidade. 
    *   ✅ **Correto:** `Assets/LumoJam/Characters/Player/`
    *   ❌ **Incorreto:** `Assets/LumoJam/Player_Files/Meshes/`
*   **PascalCase Sempre:** Todas as pastas devem ser nomeadas em `PascalCase`. Sem espaços, sem acentos, sem hífens ou underlines.
    *   ✅ **Correto:** `LevelDesign`, `UserInterface`
    *   ❌ **Incorreto:** `level_design`, `User Interface`

---

## 2. Convenção de Nomenclatura de Assets (#anc)

Nossos arquivos devem ser facilmente pesquisáveis na barra de busca da Unity. Todo asset deve seguir a estrutura:

**`Prefixo_NomeBase_Variante_Sufixo`**

### Tabela de Prefixos Oficiais

| Tipo de Asset | Prefixo | Exemplo de Uso |
| :--- | :--- | :--- |
| **Prefab** | `PF_` | `PF_InimigoAtirador` |
| **Modelo 3D (Mesh)** | `SM_` | `SM_PortaMadeira` |
| **Material** | `M_` | `M_PortaMadeira` |
| **Textura** | `T_` | `T_PortaMadeira_Albedo`, `T_PortaMadeira_Normal` |
| **Áudio (SFX / Música)** | `A_` | `A_Passo_Grama_01`, `A_TemaPrincipal` |
| **Animação (Clip)** | `Anim_` | `Anim_Player_Correndo` |
| **Controlador de Animação** | `AC_` | `AC_Player` |
| **Scriptable Object** | `DA_` | `DA_StatusEspada` (Data Asset) |

### Scripts C#
Diferente dos assets visuais, os scripts em código **não levam prefixo**. Eles devem seguir puramente o padrão `PascalCase` e ter nomes que deixem clara a sua função.
*   ✅ **Correto:** `PlayerMovement.cs`, `HealthSystem.cs`
*   ❌ **Incorreto:** `script_player.cs`, `C_Vida.cs`

---

## 3. Git e Controle de Versão

Este repositório utiliza **Git LFS** (Large File Storage) para lidar com arquivos pesados de arte e áudio. 

*   **Não altere o `.gitattributes`** sem avisar a equipe. Ele já está configurado para rastrear arquivos `.png`, `.wav`, `.fbx`, `.blend` e `.psd`.
*   O arquivo `.gitignore` já está configurado para bloquear a pasta `Library/`, arquivos de cache da Unity e pastas de IDEs (`.idea/`, `.vscode/`). Nunca force o envio desses arquivos para o repositório.

## 4. Dicas de Workflow
* Puxe as alterações (`git pull`) sempre antes de começar a trabalhar em uma cena.
* Se estiver usando Rider ou VS Code, verifique se as ferramentas externas estão corretamente linkadas em `Edit > Preferences > External Tools` e nunca faça commit dos arquivos temporários `.csproj` ou `.sln`.

Bom desenvolvimento a todos! 🚀
