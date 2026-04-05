# Canonical Metadata

To use your recipes across different apps, follow the conventions on how to name metadata in common cases:

| Key | Purpose | Example value |
|-----|---------|---------------|
| `source`, `source.name` | Where the recipe came from. Usually a URL, can also be text (e.g. a book title). | `https://example.org/recipe`, `The Palomar Cookbook <urn:isbn:9781784720995>`, `mums` |
| `author`, `source.author` | The author of the recipe. | `John Doe` |
| `source.url` | The URL of the recipe if nested format is used. | `https://example.org/recipe` |
| `servings`, `serves`, `yield` | Indicates how many people the recipe is for. Used for scaling quantities. Leading number is used for scaling, anything else is ignored but shown as units. | `2`, `15 cups worth` |
| `course`, `category` | Meal category or course. | `dinner` |
| `locale` | The locale of the recipe. Used for spelling/grammar during edits, and for pluralisation of amounts. Uses ISO 639 language code, then optionally an underscore and the ISO 3166 alpha-2 country code for dialect variants. | `es_VE`, `en_GB`, `fr` |
| `time required`, `time`, `duration` | The preparation + cook time of the recipe. Various formats can be parsed; if in doubt use `HhMm` format to avoid plurals and locales. | `45 minutes`, `1 hour 30 minutes`, `1h30m` |
| `prep time`, `time.prep` | Time for preparation steps only. | `2 hour 30 min` |
| `cook time`, `time.cook` | Time for actual cooking steps. | `10 minutes` |
| `difficulty` | Recipe difficulty level. | `easy` |
| `cuisine` | The cuisine of the recipe. | `French` |
| `diet` | Indicates a dietary restriction or guideline for which this recipe or menu item is suitable, e.g. diabetic, halal etc. | `gluten-free`, or array of values |
| `tags` | List of descriptive tags. | `[2022, baking, summer]` |
| `image`, `images`, `picture`, `pictures` | URL to a recipe image. | `https://example.org/recipe_image.jpg` or array of URLs |
| `title` | Title of the recipe. | `Uzbek Manti` |
| `introduction`, `description` | Additional notes about the recipe. | `This recipe is a traditional Uzbek dish that is made with a variety of vegetables and meat.` |