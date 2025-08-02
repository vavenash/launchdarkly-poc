# LaunchDarkly Feature Flag PoC

This repository demonstrates a simple proof-of-concept (PoC) for testing feature flag implementation using [LaunchDarkly](https://launchdarkly.com/) in Python.

## Overview

The PoC connects to LaunchDarkly using the Python SDK and evaluates a feature flag for a sample user context. It also listens for real-time changes to the flag value and prints updates to the console.

## Prerequisites

- Python 3.8+
- A LaunchDarkly account and SDK key
- The `launchdarkly-server-sdk` Python package

## Setup

1. **Install dependencies:**

   ```sh
   pip install -r requirements.txt
   ```

2. **Set your LaunchDarkly SDK key:**

   Set the environment variable `LAUNCHDARKLY_SDK_KEY` with your SDK key:

   ```sh
   export LAUNCHDARKLY_SDK_KEY=your-sdk-key
   ```

   On Windows (PowerShell):

   ```powershell
   $env:LAUNCHDARKLY_SDK_KEY="your-sdk-key"
   ```

3. **Configure your feature flag:**

   - Ensure you have a feature flag (default key: `advisor-ui-2-0`) created in your LaunchDarkly dashboard.

## Running the PoC

Run the main script:

```sh
python main.py
```

## What It Does

- Initializes the LaunchDarkly SDK.
- Evaluates the feature flag for a sample user context.
- Prints the flag value to the console.
- Listens for flag value changes and prints updates in real time.

## Customization

- To test a different feature flag, change the `feature_flag_key` variable in [`main.py`](main.py).
- To use a different user context, modify the context builder in [`main.py`](main.py).

## Files

- [`main.py`](main.py): Main script for flag evaluation and listening.
- [`requirements.txt`](requirements.txt): Python dependencies.

## License

MIT
