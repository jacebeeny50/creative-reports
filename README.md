# Creative Reports

Persona performance reports for ad creative analysis.

## View Reports

Open with a client parameter:
```
https://yourusername.github.io/creative-reports/?client=lola-blankets
```

## Local Development

Run a local server and open in browser:

```bash
cd creative-reports
python -m http.server 8000
# Open: http://localhost:8000/?client=lola-blankets
```

## Adding a New Client

1. Create folder: `data/your-client-slug/`
2. Add two files:
   - `config.json` - client settings, personas, thresholds
   - `persona-data.json` - ad performance data
3. Push to GitHub
4. Access at `?client=your-client-slug`

## Updating Client Data

1. Replace the JSON files in `data/{client}/`
2. Commit and push
3. Changes live in ~60 seconds

## File Structure

```
creative-reports/
├── index.html                      # Report template
├── data/
│   └── lola-blankets/
│       ├── config.json             # Client config
│       └── persona-data.json       # Ad data
└── README.md
```

## Config Schema

```json
{
  "client_name": "Client Name",
  "client_slug": "client-slug",
  "ad_account_id": "123456789",
  "logo_url": "https://...",
  "cpa_thresholds": {
    "good": 50,
    "mid": 100
  },
  "personas": [
    { "name": "Persona Name", "color": "#hex", "icon": "PN" }
  ]
}
```

## GitHub Pages Setup

1. Push this repo to GitHub
2. Go to Settings > Pages
3. Source: Deploy from branch
4. Branch: main / root
5. Save
