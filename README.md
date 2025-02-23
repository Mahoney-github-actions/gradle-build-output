# Gradle build results GitHub Action

A reusable set of actions to return build results in a workflow

Use as:
```yaml
jobs:
  build:
    steps:
      - uses: Mahoney-github-actions/gradle-build-output@v2
        if: always()
```

Captures:
* Test results in `test_result_files` (default `build/**/test-results/**/*.xml`)
* Files in `output_dir` on job success (default `build/artifacts`)
* Files in `failure_output_dir` on job failure (default `build`)
