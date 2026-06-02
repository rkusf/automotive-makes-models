# 🚗 Automotive Makes & Models Dataset

A comprehensive, community-friendly JSON dataset of **178 car makes** and **2,634 models** — ready to use in any automotive application.

---

## 📦 Contents

| File | Description |
|------|-------------|
| `automotive_makes_models.json` | Main dataset — makes/models dictionary + flat list |

---

## 📐 Data Structure

```json
{
  "total_makes": 178,
  "total_models": 2634,
  "makes_models": {
    "Abarth": ["124 Spider", "500", "500C", "595", "..."],
    "Audi": ["A1", "A3", "A4", "RS6", "..."],
    "...": ["..."]
  },
  "flat_list": [
    { "make": "Abarth", "model": "124 Spider" },
    { "make": "Abarth", "model": "500" },
    { "...": "..." }
  ]
}
```

### Fields

- **`makes_models`** — Object keyed by make name, values are arrays of model strings. Best for lookup/autocomplete by make.
- **`flat_list`** — Array of `{ make, model }` objects. Best for search, filtering, or loading into a database.

---

## 🚀 Usage Examples

### JavaScript / Node.js
```js
import data from './automotive_makes_models.json' assert { type: 'json' };

// Get all models for a specific make
const audiModels = data.makes_models['Audi'];
console.log(audiModels); // ['A1', 'A3', 'A4', 'RS6', ...]

// Search across all makes/models
const results = data.flat_list.filter(
  item => item.model.toLowerCase().includes('rs6')
);
```

### Python
```python
import json

with open('automotive_makes_models.json', encoding='utf-8') as f:
    data = json.load(f)

# Get all makes
makes = list(data['makes_models'].keys())

# Get models for a make
bmw_models = data['makes_models']['BMW']

# Iterate all make/model pairs
for entry in data['flat_list']:
    print(entry['make'], '-', entry['model'])
```

### PHP
```php
$data = json_decode(file_get_contents('automotive_makes_models.json'), true);
$makes = array_keys($data['makes_models']);
$vwModels = $data['makes_models']['Volkswagen'];
```

---

## 📊 Dataset Stats

| Metric | Count |
|--------|-------|
| Car Makes | 178 |
| Car Models | 2,634 |
| Format | JSON (UTF-8) |
| Last Updated | June 2026 |

---

## 💡 Use Cases

- Automotive marketplace dropdowns & autocomplete
- Vehicle listing platforms
- Car rental / fleet management systems
- Insurance or financing applications
- Data enrichment pipelines
- ML/AI training datasets for automotive NLP

---

## 🤝 Contributing

Contributions are welcome! If you spot a missing make or model:

1. Fork the repository
2. Edit `automotive_makes_models.json`
3. Make sure to update both `makes_models` and `flat_list`
4. Open a Pull Request with a brief description

Please keep entries in alphabetical order within each make.

---

## 📄 License

This dataset is released under the **MIT License** — free for personal and commercial use. See [`LICENSE`](./LICENSE) for details.

---

*Built and maintained by the open-source community. If this dataset saves you time, consider giving it a ⭐*
# automotive-makes-models
