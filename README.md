# Python JSON Telemetry Data Normalization

## Overview

This project demonstrates a Python-based solution for processing telemetry messages received in different JSON formats and transforming them into a common, standardized JSON structure.

The objective is to normalize heterogeneous input data into a unified format, ensuring consistency, simplifying downstream processing, and improving interoperability between systems.

## Project Structure

```text
deloitte-project/
├── data-1.json          # First telemetry input format
├── data-2.json          # Second telemetry input format
├── data-result.json     # Expected standardized JSON output
├── main.py              # Python transformation logic
└── README.md            # Project documentation
```

## Key Features

- Supports multiple JSON input formats.
- Extracts and maps relevant telemetry attributes.
- Normalizes different data structures into a common JSON schema.
- Produces consistent and structured JSON output.
- Designed for extensibility and future integration.

## Technologies

- Python 3
- JSON
- Git and GitHub

## Objective

To demonstrate data parsing, transformation, normalization, and Python programming skills by converting heterogeneous telemetry messages into a common JSON representation.

## Execution

```bash
python3 main.py
```

## Expected Result

The application processes the input telemetry data and generates a unified JSON output that follows the target structure defined in `data-result.json`.
