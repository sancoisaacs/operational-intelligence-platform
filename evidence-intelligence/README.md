# Evidence Intelligence Platform

Turn raw CSV files into executive insight in seconds.  
No installation. No backend. Fully offline.

---

## What This Is

Evidence Intelligence is a browser-native analytics engine that transforms raw datasets into structured operational insight instantly.

It runs entirely inside a single HTML file and requires:

- no infrastructure
- no database
- no permissions
- no installation

Designed for analysts operating in restricted environments, it enables rapid auditing, risk detection, sentiment analysis, and reporting directly from local files.

---

## Why This Exists

Most analysts are blocked not by skill, but by access.

Enterprise systems often delay insight through:
- permission bottlenecks
- BI queue backlogs
- engineering dependencies
- infrastructure requirements

This tool removes infrastructure as a prerequisite for analysis.

---

## Core Philosophy

Deterministic First. AI Second.

The platform follows a strict processing hierarchy.

### Deterministic Engine (Primary Layer)

Rule-based analysis runs first to ensure:

- instant results
- reproducibility
- auditability
- offline capability

### AI Augmentation (Optional Layer)

When enabled, AI analyzes deterministic outputs to:

- generate executive summaries
- identify cross-signal patterns
- produce recommendations

If AI is disabled, the platform remains fully functional.

---

## Key Capabilities

### Advanced Sentiment Engine
- weighted keyword scoring
- critical risk detection
- confidence scoring
- pattern ranking

### Visual Intelligence Dashboard
- sentiment distribution
- category breakdown
- severity analysis
- trend analysis
- location comparison

### Geographic Mapping
- interactive map
- automatic coordinate detection
- sentiment color-coding
- cluster visualization

### Report Engine
- deterministic summary
- optional AI insights
- executive-ready output

---

## Architecture

```
Data File
   ↓
Parser Layer
   ↓
Processing Engine
   ├ Sentiment Analysis
   ├ Pattern Detection
   ├ Confidence Scoring
   └ Classification
   ↓
Visualization Layer
   ├ Charts
   ├ Map
   └ Metrics
   ↓
Report Engine
   ├ Deterministic Summary
   ├ AI Insights (optional)
   └ Export
```

---

## Technical Stack

Core Engine: Vanilla JavaScript  
Architecture: Single File Application  
Styling: Tailwind CSS  
Charts: Chart.js  
Maps: Leaflet  
Parsing: XLSX.js  
Export: html2pdf.js  
AI: Google Gemini API  

---

## Quick Start

1. Download `index.html`
2. Open in Chrome or Edge
3. Upload dataset
4. Generate insights

No installation required.

---

## Data Format Detection

Headers are automatically recognized when they resemble:

| Field | Keywords |
|------|-----------|
Text | feedback, comment, review |
Category | category, type |
Location | location, city |
Date | date, timestamp |
Latitude | lat, latitude |
Longitude | lon, lng |

---

## Performance

Typical dataset: 5,000 rows  
Load time: <1 second  
Analysis time: <200 ms  
Memory usage: ~25 MB  

Runs fully client-side.

---

## Security Model

- No uploads
- No storage
- No tracking
- No server calls (AI disabled mode)

Closing the tab clears all data.

---

## Limitations

- Very large datasets (>50k rows) may slow rendering
- PDF export may fail inside embedded webviews
- Sentiment engine is rule-based, not ML

---

## Intended Users

- Operations analysts  
- QA investigators  
- Compliance teams  
- Support leadership  
- Internal auditors  

---

## Philosophy

> The strongest analysts are not the ones with the most access.  
> They are the ones who can extract the most insight from the least access.

---

## Maintainer

Sanco Isaacs  
Operational Intelligence Builder

---

## License

MIT License
