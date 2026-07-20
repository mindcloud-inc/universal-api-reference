# Leadboxer: Delete Custom Tracking Domain

Deletes a custom tracking domain from a dataset in Leadboxer.

```
DELETE https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/delete-custom-tracking-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/delete-custom-tracking-domain?connectionId=$CONNECTION_ID&ctd=string&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ctd": "string",
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/delete-custom-tracking-domain?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ctd` | string | yes | The custom tracking domain to delete. |
| `datasetId` | string | yes | The dataset ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `DELETE /v1/management/ctd/{{datasetId}}` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-tracking-domain.md) for the provider-specific parameters and requirements.

