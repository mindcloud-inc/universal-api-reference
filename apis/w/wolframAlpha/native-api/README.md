# Wolfram Alpha: Native API Reference

A consolidated summary of Wolfram Alpha's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://products.wolframalpha.com/api/
- **API base URL:** `https://api.wolframalpha.com`

## Authentication

### AppID

Custom AppID authentication for Wolfram|Alpha APIs using the provider-required `appid` query parameter.

### Credentials

- **AppID:** `appid` · required · Your Wolfram|Alpha AppID from the developer portal.

[Official authentication documentation](https://products.wolframalpha.com/api/documentation)

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Discover Instant Calculator Formula](actions/discover-instant-calculator-formula.md) | `GET https://www.wolframalpha.com/queryrecognizer/query.jsp` | [docs](https://products.wolframalpha.com/instant-calculators-api/documentation) |
| [Follow Async Pod URL](actions/follow-async-pod-url.md) | `GET {{asyncPodUrl}}` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Follow Recalculate URL](actions/follow-recalculate-url.md) | `GET {{recalculateUrl}}` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results](actions/get-full-results.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results Async](actions/get-full-results-async.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results by Pod ID](actions/get-full-results-by-pod-id.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results by Pod Index](actions/get-full-results-by-pod-index.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results by Pod Title](actions/get-full-results-by-pod-title.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results by Scanner](actions/get-full-results-by-scanner.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results Image Map](actions/get-full-results-image-map.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results Images](actions/get-full-results-images.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results JSON](actions/get-full-results-json.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results Plaintext](actions/get-full-results-plaintext.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Assumption and State](actions/get-full-results-with-assumption-and-state.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Assumptions](actions/get-full-results-with-assumptions.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Formats and Width](actions/get-full-results-with-formats-and-width.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Geographic Context](actions/get-full-results-with-geographic-context.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Pod State](actions/get-full-results-with-pod-state.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Scan Timeout](actions/get-full-results-with-scan-timeout.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Full Results with Unit Preferences](actions/get-full-results-with-unit-preferences.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/api/documentation) |
| [Get Instant Calculator Default](actions/get-instant-calculator-default.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/instant-calculators-api/documentation) |
| [Get LLM Result](actions/get-llm-result.md) | `GET https://www.wolframalpha.com/api/v1/llm-api` | [docs](https://products.wolframalpha.com/llm-api/documentation) |
| [Get LLM Result with Assumption](actions/get-llm-result-with-assumption.md) | `GET https://www.wolframalpha.com/api/v1/llm-api` | [docs](https://products.wolframalpha.com/llm-api/documentation) |
| [Get LLM Result with Character Limit](actions/get-llm-result-with-character-limit.md) | `GET https://www.wolframalpha.com/api/v1/llm-api` | [docs](https://products.wolframalpha.com/llm-api/documentation) |
| [Get LLM Result with Geographic Context](actions/get-llm-result-with-geographic-context.md) | `GET https://www.wolframalpha.com/api/v1/llm-api` | [docs](https://products.wolframalpha.com/llm-api/documentation) |
| [Get LLM Result with Unit Preferences](actions/get-llm-result-with-unit-preferences.md) | `GET https://www.wolframalpha.com/api/v1/llm-api` | [docs](https://products.wolframalpha.com/llm-api/documentation) |
| [Get Short Answer](actions/get-short-answer.md) | `GET /v1/result` | [docs](https://products.wolframalpha.com/short-answers-api/documentation) |
| [Get Short Answer Imperial](actions/get-short-answer-imperial.md) | `GET /v1/result` | [docs](https://products.wolframalpha.com/short-answers-api/documentation) |
| [Get Short Answer Metric](actions/get-short-answer-metric.md) | `GET /v1/result` | [docs](https://products.wolframalpha.com/short-answers-api/documentation) |
| [Get Simple Result Image](actions/get-simple-result-image.md) | `GET /v1/simple` | [docs](https://products.wolframalpha.com/simple-api/documentation) |
| [Get Simple Result Image Custom](actions/get-simple-result-image-custom.md) | `GET /v1/simple` | [docs](https://products.wolframalpha.com/simple-api/documentation) |
| [Get Simple Result with Layout Options](actions/get-simple-result-with-layout-options.md) | `GET /v1/simple` | [docs](https://products.wolframalpha.com/simple-api/documentation) |
| [Get Spoken Result](actions/get-spoken-result.md) | `GET /v1/spoken` | [docs](https://products.wolframalpha.com/spoken-results-api/documentation) |
| [Get Spoken Result Imperial](actions/get-spoken-result-imperial.md) | `GET /v1/spoken` | [docs](https://products.wolframalpha.com/spoken-results-api/documentation) |
| [Get Spoken Result Metric](actions/get-spoken-result-metric.md) | `GET /v1/spoken` | [docs](https://products.wolframalpha.com/spoken-results-api/documentation) |
| [Get Summary Box](actions/get-summary-box.md) | `GET https://www.wolframalpha.com/summaryboxes/v1/query` | [docs](https://products.wolframalpha.com/summary-boxes-api/documentation) |
| [Get Summary Box from Recognizer Path](actions/get-summary-box-from-recognizer-path.md) | `GET https://www.wolframalpha.com/summaryboxes/v1/query` | [docs](https://products.wolframalpha.com/summary-boxes-api/documentation) |
| [Include Instant Calculator Variable](actions/include-instant-calculator-variable.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/instant-calculators-api/documentation) |
| [Recognize Query](actions/recognize-query.md) | `GET https://www.wolframalpha.com/queryrecognizer/query.jsp` | [docs](https://products.wolframalpha.com/query-recognizer/documentation) |
| [Recognize Query JSON](actions/recognize-query-json.md) | `GET https://www.wolframalpha.com/queryrecognizer/query.jsp` | [docs](https://products.wolframalpha.com/query-recognizer/documentation) |
| [Recognize Query Voice Mode](actions/recognize-query-voice-mode.md) | `GET https://www.wolframalpha.com/queryrecognizer/query.jsp` | [docs](https://products.wolframalpha.com/query-recognizer/documentation) |
| [Recognize Query with Summary Box Path](actions/recognize-query-with-summary-box-path.md) | `GET https://www.wolframalpha.com/queryrecognizer/query.jsp` | [docs](https://products.wolframalpha.com/query-recognizer/documentation) |
| [Set Instant Calculator Pulldown Value](actions/set-instant-calculator-pulldown-value.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/instant-calculators-api/documentation) |
| [Set Instant Calculator Text Input](actions/set-instant-calculator-text-input.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/instant-calculators-api/documentation) |
| [Solve Instant Calculator Variable](actions/solve-instant-calculator-variable.md) | `GET /v2/query` | [docs](https://products.wolframalpha.com/instant-calculators-api/documentation) |
| [Validate Query](actions/validate-query.md) | `GET /v2/validatequery` | [docs](https://products.wolframalpha.com/api/documentation) |
