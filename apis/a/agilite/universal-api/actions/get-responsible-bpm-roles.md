# Agilite: Get Responsible BPM Roles

Retrieves responsible BPM roles from Agilite for a BPM stub.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-responsible-bpm-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-responsible-bpm-roles?connectionId=$CONNECTION_ID&processKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-responsible-bpm-roles?${params}`, {
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
| `processKey` | string | yes | Agilit-e BPM process key. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responsibleUser` | string | no | Optional responsible user filter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /bpm/getResponsibleRoles` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-responsible-bpm-roles.md) for the provider-specific parameters and requirements.

