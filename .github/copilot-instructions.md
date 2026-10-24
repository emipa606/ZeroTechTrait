# GitHub Copilot Instructions for ZeroTech-Trait Mod

## Mod Overview and Purpose

**ZeroTech-Trait (Continued)** is a RimWorld mod that updates and expands the LingLuos mod. It introduces a set of new traits that enhance player characters' attributes and behaviors, providing a unique experience for RimWorld players.

## Key Features and Systems

### Traits
- **Immune Deficiency:** Low immunity to diseases.
- **Mental Mania:** Random thoughts and behaviors.
- **Worthless:** Very low value in social interactions.
- **Cold Physique:** Sensitive to cold environments.
- **Heat Fear Physique:** Sensitive to hot environments.
- **Leverage:** Prone to causing conflicts.
- **Math Idiot:** Poor calculation skills.
- **Body Deformities:** Weak mobility and unattractive appearance.
- **Arrogance:** Difficulty in learning and adapting.
- **Greedy:** Craves multiple romantic partners.

### Coding Patterns and Conventions

- **C# Code Structure:** 
  - The mod uses a clear and organized structure with separate files for different types of code (e.g., ThoughtWorker, InteractionWorker).
  - Each file typically contains a single class with well-defined methods.
- **XML Integration:**
  - XML files are used for defining traits, thoughts, and interactions.
  - Each XML file has a corresponding C# file for integration.

### Harmony Patching

- **Harmony Patching:**
  - The mod uses Harmony for patching vanilla RimWorld methods to introduce new behaviors.
  - Patches are located in the `ZeroTechTraitDefOf.cs` and other relevant files.

## XML Integration

### XML Files

- **Traits_Singular.xml:** Contains definitions for new traits.
- **About.xml:** Contains metadata about the mod.
- **TranslationTemplate:** Contains XML templates for translations in different languages (Simplified Chinese, English).

## Harmony Patching

### Harmony Patches

- **ThoughtWorker_NeedLover.cs:** Contains a patch for the `ThoughtWorker_NeedLover` class.
- **InteractionWorker_Nonsense.cs:** Contains a patch for the `InteractionWorker_Nonsense` class.

## Suggestions for Copilot

### General Guidelines

- **Consistent Naming:** Use consistent naming conventions for classes, methods, and variables.
- **Documentation:** Write clear and concise comments for each method and class.
- **Code Reusability:** Use code reusability techniques to avoid duplication.

### Specific Suggestions

- **C# Code:**
  - When writing new C# code, use existing classes and methods as templates.
  - Ensure that new classes and methods follow the established patterns and conventions.

- **XML Code:**
  - When writing new XML code, refer to existing XML files for the correct structure and formatting.
  - Ensure that XML tags and attributes are correctly spelled and capitalized.

## Example Workflow

1. **Create a New Trait:**
   - Open `Traits_Singular.xml` and add a new trait definition.
   - Create a new C# class for the trait and implement any necessary methods.
   - Use Copilot to generate the initial code and then refine it according to the established conventions.

2. **Implement a Harmony Patch:**
   - Identify the vanilla method that needs to be patched.
   - Use Copilot to generate the initial patch code.
   - Refine the patch code to ensure that it correctly implements the desired behavior.

3. **Test the Mod:**
   - Use RimSort to sort the mods and ensure that they are loaded correctly.
   - Test the new trait and patch in a RimWorld game to ensure that they work as expected.

By following these guidelines and suggestions, you can effectively use GitHub Copilot to enhance and maintain the ZeroTech-Trait mod for RimWorld.

## Project Solution Guidelines
- Relevant mod XML files are included as Solution Items under the solution folder named XML, these can be read and modified from within the solution.
- Use these in-solution XML files as the primary files for reference and modification.
- The `.github/copilot-instructions.md` file is included in the solution under the `.github` solution folder, so it should be read/modified from within the solution instead of using paths outside the solution. Update this file once only, as it and the parent-path solution reference point to the same file in this workspace.
- When making functional changes in this mod, ensure the documented features stay in sync with implementation; use the in-solution `.github` copy as the primary file.
- In the solution is also a project called Assembly-CSharp, containing a read-only version of the decompiled game source, for reference and debugging purposes.
- For any new documentation, update this copilot-instructions.md file rather than creating separate documentation files.


## Hard rules (must follow)
- Do NOT run commands that modify the repo (no git commit, git apply, dotnet format) unless explicitly asked.
- Prefer minimal reads: read only the smallest code region needed (around the suspicious lines).
- When mentioning SonarQube issues, automatically use the SonarQube MCP service to fetch and address issues instead of making inferred fixes without querying SonarQube first.
- When mentioning the rimworld log, automatically use the Rimworld MCP service to fetch the log.

