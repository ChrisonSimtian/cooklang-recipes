# Cooklang Conventions

This workspace contains recipes in [Cooklang](https://cooklang.org/) format. Follow these rules when creating or editing `.cook` files.

## Language & Folder Structure

- German recipes go into the `Deutsche Gerichte/` folder.
- Non-English recipes: translate all folder names, comments, and step text into the recipe's language (e.g. "Sauces" → "Soßen", "Self Made" → "Selbstgemacht", "Mains" → "Hauptgerichte").
- Sauces go into a `Sauces/` subfolder (or language equivalent, e.g. `Soßen/`).
- Items that are ingredients themselves (pasta, bread, etc.) go into a `Self Made/` subfolder (or language equivalent, e.g. `Selbstgemacht/`).
- Main dishes go into a `Mains/` subfolder (or language equivalent, e.g. `Hauptgerichte/`).

## Cooklang Syntax

- Use `@ingredient{quantity%unit}` for ingredients, `#cookware{}` for cookware, `~{time%unit}` for timers.
- When an ingredient can be substituted (e.g. Wasser/Bier/Milch), pick one as the `@ingredient{}` and add a `--` comment noting the alternatives.
- Before creating a recipe, check the workspace for existing `.cook` files that match an ingredient. If found, link to it using a relative path: `@./Soßen/Hollandaise{150%g}`.

## Metadata

- Always add meaningful metadata using YAML front matter (between `---` dashes).
- Add the `locale` tag to define the language using **ISO 639 + ISO 3166 alpha-2** (e.g. `de_DE`, `en_GB`).
- Add the `course` tag to every course (main dish, breakfast, etc.) and the `category` tag to everything else (sides, salads, sauces, etc.).
- Calculate the overall time and add it as a tag.
- Add descriptive `tags` (e.g. pasta, baking, summer).
- Respect the [Canonical Metadata](canonical-metadata.md) for key names and formats.

## Workflow

- When a recipe is pasted, automatically convert it into a `.cook` file following all rules above.
- The first line of the pasted text is the recipe name and becomes the filename.
- Place the file in the correct subfolder based on its type and language.