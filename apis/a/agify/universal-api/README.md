# <img src="https://images.mindcloud.co/apps/icons/agify_1785426332416.png" alt="Agify logo" width="28" height="28"> Agify: Universal API

Predict a statistical age estimate from a first or full name, optionally scoped to a country.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agify/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agify.io/
- **Vendor API docs:** https://agify.io/documentation/api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Predict Age](actions/predict-age.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agify/latest/actions/predict-age?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Age Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Predict Age](actions/predict-age.md) | GET |  |

### Age Predictions

| Action | Method | Description |
| --- | --- | --- |
| [Predict Ages](actions/predict-ages.md) | GET |  |

