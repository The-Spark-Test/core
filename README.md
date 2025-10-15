# SPARK Core

## Overview

The **SPARK Core** repository contains the foundational logic, algorithms, and data models for the Skill Performance Assessment for Robotics Kinetics (SPARK) framework. It defines the computational backbone for robotic motion analysis, performance metrics, and evaluation scoring.

## Features

- Core algorithms for performance scoring and skill quantification
- Standardized data structures for metrics and evaluation results
- Mathematical models for motion, balance, and kinetics
- Integration points with the `evaluation`, `simulator`, and `robot-interface` modules

## Architecture

```
core/
├── spark/
│   ├── metrics/          # Metric definitions and scoring formulas
│   ├── analysis/         # Core algorithms for performance evaluation
│   ├── models/           # Data models and serialization logic
│   ├── utils/            # Shared utility functions
│   └── __init__.py
├── tests/                # Unit and integration tests
└── main.py               # Entry point for running core tests
```

## Tech Stack

- **Language:** Python 3.11+
- **Libraries:** NumPy, SciPy, Pandas, Scikit-learn
- **Testing:** PyTest

## Installation

```bash
# Clone the repository
git clone <repository-url>
cd spark_core

# Install dependencies
pip install -r requirements.txt

# Run tests
python -m pytest tests/
```

## Usage

```python
from spark import metrics, analysis, models

# Example usage
performance_data = models.PerformanceData(...)
score = analysis.calculate_performance_score(performance_data)
```

## Integration

The Core layer acts as the computational engine for:

- `evaluation/` → Uses scoring logic
- `simulator/` → Retrieves motion data for analysis
- `api/` → Exposes endpoints using the Core API models

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

## License

[Add license information here]
