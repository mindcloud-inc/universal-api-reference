# <img src="https://images.mindcloud.co/apps/icons/wolfram-alpha-icon-final_1776351500996.png" alt="Wolfram Alpha logo" width="28" height="28"> Wolfram Alpha: Universal API

Access Wolfram|Alpha’s computational knowledge APIs for full results, short answers, spoken responses, simple images, query recognition, summary boxes, and LLM-oriented responses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wolframAlpha/latest
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wolframalpha.com/
- **Vendor API docs:** https://products.wolframalpha.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Short Answer](actions/get-short-answer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-short-answer?connectionId=$CONNECTION_ID&i=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Formula

| Action | Method | Description |
| --- | --- | --- |
| [Discover Instant Calculator Formula](actions/discover-instant-calculator-formula.md) | GET | Discovers an instant calculator formula in Wolfram Alpha. |
| [Get Instant Calculator Default](actions/get-instant-calculator-default.md) | GET | Retrieves a default instant calculator from Wolfram Alpha. |
| [Include Instant Calculator Variable](actions/include-instant-calculator-variable.md) | GET | Retrieves a Wolfram Alpha instant calculator with an included variable. |
| [Set Instant Calculator Pulldown Value](actions/set-instant-calculator-pulldown-value.md) | GET | Retrieves a Wolfram Alpha instant calculator with a selected pulldown value. |
| [Set Instant Calculator Text Input](actions/set-instant-calculator-text-input.md) | GET | Retrieves a Wolfram Alpha instant calculator with a text input value. |
| [Solve Instant Calculator Variable](actions/solve-instant-calculator-variable.md) | GET | Retrieves a Wolfram Alpha instant calculator solved for a variable. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Simple Result Image Custom](actions/get-simple-result-image-custom.md) | GET | Retrieves a custom simple result image from Wolfram Alpha. |
| [Get Simple Result with Layout Options](actions/get-simple-result-with-layout-options.md) | GET | Retrieves a simple Wolfram Alpha result image with layout options. |

### Pod

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Results by Pod ID](actions/get-full-results-by-pod-id.md) | GET | Retrieves Wolfram Alpha results for a specific pod ID. |
| [Get Full Results by Pod Index](actions/get-full-results-by-pod-index.md) | GET | Retrieves Wolfram Alpha results for a specific pod index. |
| [Get Full Results by Pod Title](actions/get-full-results-by-pod-title.md) | GET | Retrieves Wolfram Alpha results for a specific pod title. |
| [Get Full Results by Scanner](actions/get-full-results-by-scanner.md) | GET | Retrieves Wolfram Alpha results for a specific scanner. |
| [Get Full Results with Pod State](actions/get-full-results-with-pod-state.md) | GET | Retrieves full Wolfram Alpha query results with a pod state. |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Follow Async Pod URL](actions/follow-async-pod-url.md) | GET | Retrieves an asynchronous pod result from Wolfram Alpha. |
| [Follow Recalculate URL](actions/follow-recalculate-url.md) | GET | Retrieves recalculated results from a Wolfram Alpha query URL. |
| [Get Full Results](actions/get-full-results.md) | GET | Retrieves full Wolfram Alpha query results. |
| [Get Full Results Async](actions/get-full-results-async.md) | GET | Retrieves full Wolfram Alpha query results asynchronously. |
| [Get Full Results Image Map](actions/get-full-results-image-map.md) | GET | Retrieves full Wolfram Alpha query results with image maps. |
| [Get Full Results Images](actions/get-full-results-images.md) | GET | Retrieves full Wolfram Alpha query results with images. |
| [Get Full Results JSON](actions/get-full-results-json.md) | GET | Retrieves full Wolfram Alpha query results in JSON. |
| [Get Full Results Plaintext](actions/get-full-results-plaintext.md) | GET | Retrieves full Wolfram Alpha query results in plaintext. |
| [Get Full Results with Assumption and State](actions/get-full-results-with-assumption-and-state.md) | GET | Retrieves full Wolfram Alpha query results with assumptions and pod state. |
| [Get Full Results with Assumptions](actions/get-full-results-with-assumptions.md) | GET | Retrieves full Wolfram Alpha query results with assumptions. |
| [Get Full Results with Formats and Width](actions/get-full-results-with-formats-and-width.md) | GET | Retrieves full Wolfram Alpha query results with custom formats and width. |
| [Get Full Results with Geographic Context](actions/get-full-results-with-geographic-context.md) | GET | Retrieves full Wolfram Alpha query results with geographic context. |
| [Get Full Results with Scan Timeout](actions/get-full-results-with-scan-timeout.md) | GET | Retrieves full Wolfram Alpha query results with a scan timeout. |
| [Get Full Results with Unit Preferences](actions/get-full-results-with-unit-preferences.md) | GET | Retrieves full Wolfram Alpha query results with unit preferences. |
| [Get LLM Result](actions/get-llm-result.md) | GET | Retrieves an LLM-ready result from Wolfram Alpha. |
| [Get LLM Result with Assumption](actions/get-llm-result-with-assumption.md) | GET | Retrieves an LLM-ready Wolfram Alpha result with assumptions. |
| [Get LLM Result with Character Limit](actions/get-llm-result-with-character-limit.md) | GET | Retrieves an LLM-ready Wolfram Alpha result with a character limit. |
| [Get LLM Result with Geographic Context](actions/get-llm-result-with-geographic-context.md) | GET | Retrieves an LLM-ready Wolfram Alpha result with geographic context. |
| [Get LLM Result with Unit Preferences](actions/get-llm-result-with-unit-preferences.md) | GET | Retrieves an LLM-ready Wolfram Alpha result with unit preferences. |
| [Get Short Answer](actions/get-short-answer.md) | GET | Retrieves a short text answer from Wolfram Alpha. |
| [Get Short Answer Imperial](actions/get-short-answer-imperial.md) | GET | Retrieves a short imperial answer from Wolfram Alpha. |
| [Get Short Answer Metric](actions/get-short-answer-metric.md) | GET | Retrieves a short metric answer from Wolfram Alpha. |
| [Get Simple Result Image](actions/get-simple-result-image.md) | GET | Retrieves a simple result image from Wolfram Alpha. |
| [Get Spoken Result](actions/get-spoken-result.md) | GET | Retrieves a spoken-style text answer from Wolfram Alpha. |
| [Get Spoken Result Imperial](actions/get-spoken-result-imperial.md) | GET | Retrieves a spoken imperial answer from Wolfram Alpha. |
| [Get Spoken Result Metric](actions/get-spoken-result-metric.md) | GET | Retrieves a spoken metric answer from Wolfram Alpha. |
| [Validate Query](actions/validate-query.md) | GET | Validates whether a Wolfram Alpha query can be processed. |

### Recognition

| Action | Method | Description |
| --- | --- | --- |
| [Recognize Query](actions/recognize-query.md) | GET | Recognizes whether Wolfram Alpha can process a query. |
| [Recognize Query JSON](actions/recognize-query-json.md) | GET | Recognizes a query in Wolfram Alpha and returns JSON. |
| [Recognize Query Voice Mode](actions/recognize-query-voice-mode.md) | GET | Recognizes a query in Wolfram Alpha voice mode. |
| [Recognize Query with Summary Box Path](actions/recognize-query-with-summary-box-path.md) | GET | Recognizes a query and returns a Wolfram Alpha summary box path. |

### Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Summary Box](actions/get-summary-box.md) | GET | Retrieves a summary box from Wolfram Alpha. |
| [Get Summary Box from Recognizer Path](actions/get-summary-box-from-recognizer-path.md) | GET | Retrieves a Wolfram Alpha summary box from a recognizer path. |

