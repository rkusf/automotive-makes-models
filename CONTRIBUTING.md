# Contributing to Automotive Makes & Models Dataset

Thank you for helping keep this dataset accurate and up to date! 🙌

---

## How to Contribute

### Reporting Missing or Incorrect Data

1. Open an [Issue](../../issues/new) and use the title format:
   - `[ADD] Make - Model` — for missing entries
   - `[FIX] Make - Model` — for incorrect entries
   - `[REMOVE] Make - Model` — for entries that no longer exist

2. Include a brief justification or reference if possible.

### Submitting a Pull Request

1. **Fork** this repository
2. **Edit** `automotive_makes_models.json`:
   - Add the make to `makes_models` (keep alphabetical order)
   - Add corresponding entries to `flat_list`
   - Update `total_makes` and/or `total_models` counts
3. **Validate** your JSON (e.g. `python3 -m json.tool automotive_makes_models.json`)
4. **Open a PR** with a clear title and description

### JSON Validation (quick check)

```bash
python3 -m json.tool automotive_makes_models.json > /dev/null && echo "✅ Valid JSON"
```

---

## Guidelines

- Keep make and model names in their **official/common market spelling**
- Use **UTF-8** encoding for special characters (e.g., accented brand names)
- Do not add duplicate entries
- When in doubt about a model name, prefer the most widely used variant

---

## Code of Conduct

Be respectful and constructive. This is a collaborative community project.
