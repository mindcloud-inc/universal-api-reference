# <img src="https://images.mindcloud.co/apps/icons/80694982_1776450858798.png" alt="Muna logo" width="28" height="28"> Muna: Universal API

Build and run Muna predictors and inspect predictor metadata via the Muna REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/muna/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.muna.ai/
- **Vendor API docs:** https://docs.muna.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Predictor](actions/retrieve-predictor.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/muna/latest/actions/retrieve-predictor?connectionId=$CONNECTION_ID&tag=my-predictor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Prediction](actions/create-prediction.md) | POST | Creates a prediction in Muna for a predictor tag. |
| [Retrieve Predictor](actions/retrieve-predictor.md) | GET | Retrieves a predictor from Muna by tag. |

