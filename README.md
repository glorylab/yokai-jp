# Open Dataset of Japanese Yokai

An **experimental open dataset** of Japanese Yokai (妖怪) for cultural, educational, and creative uses.  
Maintained by the team behind **[YOKAI.JP](https://yokai.jp)** - a Japanese yokai culture portal featuring an encyclopedia, interactive experiences, and editorial content.

> **Important:** This dataset mirrors the content structure and entries available at **https://yokai.jp/yokai**.  
> It is provided for reference and experimentation only.

---

## About YOKAI.JP

**YOKAI.JP** is a comprehensive **Japanese yokai culture portal**. It presents a browsable yokai encyclopedia (traditional & modern), an interactive **[Yokai Diagnosis](https://yokai.jp/diagnosis)** quiz, an online **[Yokai Shrine](https://yokai.jp/shrine)** (omikuji, ema, visit flow), and [kid-friendly pages](https://kids.yokai.jp). The site also publishes frequently updated **Daily Yokai** entries and other interactive features.

This repository provides a machine-readable extract of that yokai catalog.

---

## Status & Disclaimers

- **Language:** Currently **Japanese only** (`metadata.language = "ja"`).  
  English and other languages will be added in future releases.

- **Stability:** The dataset is **unstable**. Field names, structures, IDs, and content **may change at any time**.  
  Treat this as a **prototype/reference**, not a production API.

- **Accuracy & Scope:** Traditional yokai vary by region, source, and era.  
  Entries **are not academically authoritative** and may be incomplete or simplified.  
  **Do not use for rigorous scholarship or serious factual claims.** This is a cultural dataset intended for exploration.

- **Alignment:** The data **tracks** the content at **yokai.jp/yokai**; when the site evolves, this dataset may follow.

- **Types (`yokaiType`):**
  - `traditional` — entities drawn from folklore, classical texts, and historical imagery  
  - `daily` — modern yokai **created by YOKAI.JP** for contemporary/interactive contexts

- **Roadmap:** Upcoming versions may add **source citations (出典)**, extended references, and richer metadata.

---

## Data Model (overview)

Top-level fields (example from `metadata` in `v0.1.0`):

```json
{
  "metadata": {
    "language": "ja",
    "version": "0.1.0",
    "generatedAt": "2025-09-09T06:44:28.749Z",
    "totalSpecies": 141,
    "totalVersions": 145,
    "totalImages": 156,
    "description": "YOKAI.JP Open Dataset - Japanese Yokai Species and Versions",
    "license": "CC BY-SA 4.0",
    "sourceUrl": "https://yokai.jp",
    "githubUrl": "https://github.com/glorylab/yokai-jp"
  }
}
```

Each item in `species[]` typically includes:

- `slug` — stable identifier (e.g., karakasa-kozou)
- `name` — primary Japanese name
- `nameKana` — reading
- `aliases[]` — alternative names (optionally with readings)
- `category` — loose classification
- `yokaiType` — traditional or original
- `origin` — brief provenance (when applicable)
- `baseDescription` — short description (JP)
- `versions[]` — variant records (e.g., traditional iconography vs. modern reinterpretation)
  - `slug`, `versionName`, `description`, etc.

> Note: Field presence and semantics may evolve as the site evolves.

## Use Cases

- Cultural/educational apps or demos
- Creative coding and prototyping (cards, quizzes, timelines)
- Language learning experiments (kana, aliases)
- Lightweight NLP/playful analysis of folklore terms

For long-form articles, illustrations, and interactive experiences, please visit [yokai.jp](https://yokai.jp).

## License

Creative Commons Attribution–ShareAlike 4.0 (CC BY-SA 4.0)

You may share and adapt the data with attribution and under the same license.

See the full legal text: https://creativecommons.org/licenses/by-sa/4.0/

Attribution example:
“Data from YOKAI.JP – Open Dataset of Japanese Yokai (CC BY-SA 4.0).”

## Contributing

Contributions are welcome — corrections (readings/aliases), additions, translations, or ideas for structure.

Please open an Issue or submit a Pull Request.

Because the dataset mirrors site content, structural changes may be considered on a case-by-case basis.

## Contact

For inquiries (including commercial or partnership questions), please reach out via [yokai.jp/contact](https://yokai.jp/contact).
