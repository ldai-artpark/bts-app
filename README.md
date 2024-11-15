# VAANI ASR Analysis Dashboard

A Streamlit dashboard for analyzing Word Error Rate (WER) metrics across Karnataka districts for ASR models.

## Features

- Interactive Karnataka map with district-wise WER visualization 
- Color-coded districts based on WER thresholds
- Audio sample analysis with transcription comparison
- Model performance metrics and district-wise breakdown

## Setup

### Prerequisites

```bash
python -3.8 or higher
```

### Project Structure
```
project/
├── app.py              # Main application file
├── requirements.txt    # Python dependencies
├── data/              # Data files
│   └── sample2.json   # Sample data
└── logo/              # Logo assets
    ├── ARTPARK.png
    ├── IISC.png 
    ├── google.png
    └── bhashini.png
```

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/vaani-dashboard.git
cd vaani-dashboard
```

2. Install dependencies
```bash 
pip install -r requirements.txt
```

3. Run the application
```bash
streamlit run app.py
```

## Usage

1. The dashboard loads with an interactive map of Karnataka
2. Districts are color-coded based on WER:
   - Green: WER ≤ 20%
   - Orange: 20% < WER ≤ 50% 
   - Red: WER > 50%

3. Click on a district or use the dropdown to view:
   - District WER score
   - Audio samples with transcriptions
   - Model output vs reference text

## Data Format

Sample JSON structure:
```json
{
  "Model_1": {
    "District1": {
      "WER": "50.55",
      "Samples": {
        "Sample_1": {
          "URL": "audio_url",
          "ModelOutput": "model transcription",
          "Reference": "reference text"
        }
      }
    }
  }
}
```

## Dependencies

```
streamlit==1.29.0
folium==0.14.0
streamlit-folium==0.15.0
pandas==2.1.3
requests==2.31.0
shapely==2.0.2
```

## License

MIT License

## Acknowledgments

Supported by:
- Google
- Bhashini
- ARTPARK
- IISc