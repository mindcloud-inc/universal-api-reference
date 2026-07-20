# Leadboxer: Add Custom Tracking Domain

Creates a custom tracking domain in Leadboxer and starts certificate generation.

```
POST https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-custom-tracking-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-custom-tracking-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ctd": "string",
  "datasetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/add-custom-tracking-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ctd": "string",
    "datasetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ctd` | string | yes | The custom tracking domain to add. |
| `datasetId` | string | yes | The dataset ID. |
| `description` | string | no | Optional description for the custom tracking domain. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `POST /v1/management/ctd/add` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-tracking-domain.md) for the provider-specific parameters and requirements.

