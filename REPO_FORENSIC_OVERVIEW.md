# Repository Forensic Overview

This document captures a code-first forensic understanding of the project architecture, stack, and behavior for interview preparation.

Key findings:
- FastAPI app exposes upload/status/result endpoints.
- Celery + Redis powers async processing.
- Pipeline reads Excel files, profiles data, computes top correlations, and writes JSON artifacts.
- Dashboard HTML is generated from analysis JSON.
- Groq LLM call generates structured insights JSON.
- Optional SMTP email task sends dashboard + analysis attachments.

See source files under `autoAnalysis/app/` for implementation details.
