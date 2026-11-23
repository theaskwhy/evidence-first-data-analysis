---
name: evidence-first-data-analysis
description: Analyze and validate datasets with reproducible, evidence-backed methods. Read-only by default; never fabricate metrics or perform data writes.
---

# Evidence-First Data Analysis

Use connected structured data, datasets supplied by the user, or explicitly disclosed public sources. Do not claim access to financial, business, or warehouse data without actual access.

## Choose the deliverable

- For a metric or comparison, identify the business question, grain, timeframe, filters, authoritative field definitions, and decision threshold.
- For a trustworthy analysis, check freshness, duplicates, key coverage, joins, missingness, leakage, denominators, and data quality before explaining trends.
- For a dashboard or report, publish only source-backed figures. Identify lineage, refresh time, and security controls. Never substitute realistic-looking fabricated data in production analysis.
- For a query, show intended read-only SQL and estimated volume/sample before execution when possible. Avoid DML/DDL, unbounded scans, write-query analysis, or privileged data dumps by default.

## Required checks

1. Confirm permission and source provenance. Mask or aggregate identifying or financial account data; never echo secrets. Avoid individual records when grouped data suffices.
2. Prefer local or low-cost operations and protect shared quotas. No paid services without explicit approval.
3. Validate counts, units, time zones, denominators, join multiplicity, null handling, and alternative explanations. Do not infer causation from correlation.
4. Independently verify decisive calculations and include uncertainty or confidence bounds where warranted.
5. If data is absent, return `NO_DATA` with the exact missing input and a plan. Do not invent benchmarks or present modeled values as facts.
6. Never render unescaped content-derived HTML. External dependencies or sensitive data exports require review.

## Report

State the question, scope, data owner/source identifiers, extraction or query time, and whether a real query was executed or only proposed. Define metrics, periods, units, denominators, and groups. Present supported findings and quality results with `PASS`, `FAIL`, `NOT_RUN`, or `NO_DATA`; never claim a check passed if it was not performed. Cite source records precisely without exposing sensitive data. Before sharing, apply `references/data-quality-checklist.md` and report outstanding checks and approvals.

## Write boundary

Database tools can be write-capable despite names such as “query.” Treat `INSERT`, `UPDATE`, `DELETE`, `CREATE`, `DROP`, `ALTER`, state-changing `PRAGMA`, `MERGE`, stored procedures, and multi-statements as writes. Before any backend action, review the exact target, credentials, account, query, and permissions. In ambiguous cases, use an isolated local test or abstain. Live SQL behavior and role permissions remain `NOT_RUN` until verified.
