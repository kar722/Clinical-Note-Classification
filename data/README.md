# Clinical Notes Classification Dataset

This is a synthetic dataset created for developing and testing clinical note classification systems. The dataset follows the format of the n2c2 2010 dataset.

## Directory Structure
```
data/
├── train/          # Training data (70% of samples)
├── dev/            # Development/Validation data (10% of samples)
└── test/           # Test data (20% of samples)
```

## File Format
Each clinical note has 4 associated files:
- `.txt`: The clinical note text
- `.con`: Concept annotations (problems, tests, treatments)
- `.ast`: Assertion annotations for medical problems
- `.rel`: Relation annotations between concepts

## Annotation Guidelines

### Concept Types (in .con files)
- problem: Medical problems, symptoms, conditions
- test: Diagnostic procedures, lab tests, imaging
- treatment: Medications, procedures, interventions

### Assertion Types (in .ast files)
- present: Condition is present
- absent: Condition is explicitly negated
- possible: Condition is uncertain
- conditional: Condition is hypothetical
- associated_with_someone_else: Condition relates to someone other than patient
- hypothetical: Condition is discussed as a hypothetical scenario

### Relation Types (in .rel files)
- TrAP: Treatment administered for Problem
- TrCP: Treatment causes Problem
- TrNAP: Treatment not administered because of Problem
- TrWP: Treatment worsens Problem
- TeRP: Test reveals Problem
- TeCP: Test conducted to investigate Problem
- PIP: Problem indicates Problem

## Statistics
- Total samples: 30
- Training samples: 21
- Development samples: 3
- Test samples: 6 