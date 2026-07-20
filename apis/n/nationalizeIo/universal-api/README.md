# <img src="https://images.mindcloud.co/apps/icons/favicon-nationalize-io-48x48_1777546262963.png" alt="Nationalize_io logo" width="28" height="28"> Nationalize_io: Universal API

Predicts the likely nationality of a name using Nationalize.io's public statistical name-nationality API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nationalizeIo/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nationalize.io
- **Vendor API docs:** https://nationalize.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Predict Nationality by Name](actions/predict-nationality-by-name.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalizeIo/latest/actions/predict-nationality-by-name?connectionId=$CONNECTION_ID&name=johnson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Nationality Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Predict Nationalities for Names](actions/predict-nationalities-for-names.md) | GET | Retrieves nationality predictions from Nationalize.io for up to 10 names. |
| [Predict Nationality by Name](actions/predict-nationality-by-name.md) | GET | Retrieves nationality predictions from Nationalize.io for one name. |

