# Netflix Data Analysis with Apache Beam

## Project Overview
This project implements a comprehensive data analysis pipeline for Netflix shows dataset using Apache Beam, along with exploratory data analysis (EDA) and visualizations. The implementation demonstrates various Apache Beam features including composite transforms, pipeline I/O, triggers, windowing, and streaming capabilities.


## Features Implemented

### 1. Apache Beam Pipeline
- **Composite Transforms**
  - Genre Analysis Transform
  - Type Analysis Transform
  - Rating Analysis Transform

- **Pipeline I/O**
  - CSV file reading
  - JSONL file writing
  - Multiple output handling

- **Windowing & Triggers**
  - Fixed Windows implementation
  - Watermark triggers
  - Basic windowing strategy

- **ParDo Operations**
  - CSV parsing
  - Data cleaning
  - Timestamp handling

### 2. Data Analysis Components
- Content type distribution analysis
- Genre frequency analysis
- Rating distribution analysis
- Temporal analysis of content additions

## Technologies Used
- Apache Beam
- Python 3.x
- Pandas
- D3.js (for visualizations)
- Jupyter Notebooks

## Installation and Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd netflix-analysis
```

2. Install required packages:
```bash
pip install apache-beam pandas jupyter
```

3. Run the Jupyter notebook:
```bash
jupyter notebook notebooks/netflix_beam_pipeline.ipynb
```

## Pipeline Components

### 1. Data Parsing (ParseCSV)
```python
class ParseCSV(beam.DoFn):
    def process(self, element):
        # Parses CSV records into structured format
```

### 2. Analysis Transforms
```python
class GenreAnalysis(beam.PTransform):
    def expand(self, pcoll):
        # Implements genre analysis logic

class TypeAnalysis(beam.PTransform):
    def expand(self, pcoll):
        # Implements content type analysis logic
```

### 3. Pipeline Execution
```python
def run_netflix_pipeline(input_path, output_path):
    # Main pipeline execution logic
```

## Analysis Results

### Sample Output Format
```json
{
    "genre": "Drama",
    "count": 2000,
    "window": "fixed_30s"
}
```

### Key Insights
- Distribution of content types (Movies vs TV Shows)
- Most common genres
- Rating distributions
- Content addition patterns

## Future Improvements
1. Implement real-time streaming capabilities
2. Add more complex windowing strategies
3. Enhance visualization components
4. Add more sophisticated analysis transforms
5. Implement ML components using BeamML

## Contributing
Feel free to submit issues and enhancement requests.

## Acknowledgments
- Dataset source: Kaggle Netflix Shows Dataset
- Apache Beam documentation and community
- Course instructors and peers for guidance
