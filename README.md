# Creative Reports

Ad creative intelligence reports.

## URL Structure

```
/                                    # Client selector
/clients/lola-blankets/              # Client hub (all reports)
/templates/persona-performance.html  # Report template (needs ?client=)
```

## File Structure

```
creative-reports/
├── index.html                       # Client selector
├── templates/
│   └── persona-performance.html     # Report templates
├── clients/
│   └── lola-blankets/
│       ├── index.html               # Client hub page
│       ├── config.json              # Client config
│       └── persona-data.json        # Ad performance data
└── README.md
```

## Adding a New Client

1. Create folder: `clients/your-client-slug/`
2. Copy from existing client:
   - `index.html` - Update client name and links
   - `config.json` - Client settings, personas, thresholds
   - `persona-data.json` - Ad performance data
3. Update root `index.html` to add client card
4. Push to GitHub

## Updating Reports

**Update template design:**
1. Edit `templates/persona-performance.html`
2. Commit and push

**Update client data:**
1. Replace JSON files in `clients/{client}/`
2. Commit and push

Changes live in ~60 seconds.
