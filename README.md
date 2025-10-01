FlakyFixer – CI/CD Flaky Test Eliminator

Tagline : Detect, Debug, and Fix Flaky Tests Automatically


Problem Statement

  In software development, flaky tests are tests that sometimes pass and sometimes fail, even when nothing in the code has changed.

  They create several issues:

  Developers waste time re-running pipelines to check if failures are real.

  CI/CD resources (build servers, compute time) get consumed by repeated runs.

  Confidence in automated testing decreases, slowing product delivery.

  Most existing solutions only identify flaky tests. They do not reproduce failures or suggest fixes, leaving developers to perform extra manual work.


Proposed Solution – FlakyFixer

FlakyFixer is a CI-integrated tool that:

  Detects failing or flaky tests directly from CI pipelines.

  Automatically re-runs those tests in clean, isolated Docker environments.

  Uses delta debugging to identify the minimal conditions that reproduce failures.

  Classifies root causes such as order dependency, randomness, timing issues, or external API calls.

  Generates an automated Pull Request with a reproducible script and suggested fix.


Benefits:

  Saves valuable developer time

  Reduces wasted CI/CD costs

  Restores confidence in automated testing pipelines


Tech Stack

  Languages & Frameworks: Python (FastAPI), Pytest

  Containerization & CI/CD: Docker, GitHub Actions, PyGithub API

  Debugging Techniques: Delta Debugging, Heuristic Rules

  Hosting: Cloud / VPS for orchestrator


Future Scope

  Support for multi-language testing (Java, Go, etc.)

  Machine Learning model for smarter root-cause detection

  Slack/Jira integration for team notifications

  Dashboard for test health metrics

