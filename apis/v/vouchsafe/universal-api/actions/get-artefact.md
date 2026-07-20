# Vouchsafe: Get Artefact

Retrieves an artefact download link from Vouchsafe.

```
GET https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/get-artefact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/get-artefact?connectionId=$CONNECTION_ID&artefactKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "artefactKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/get-artefact?${params}`, {
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
| `artefactKey` | string | yes | The artefact key to exchange for a presigned download URL. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `GET /artefacts/:artefact_key` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-artefact.md) for the provider-specific parameters and requirements.

