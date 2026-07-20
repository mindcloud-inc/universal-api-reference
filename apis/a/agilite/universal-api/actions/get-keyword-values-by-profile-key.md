# Agilite: Get Keyword Values By Profile Key

Retrieves keyword values from Agilite by profile key.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-values-by-profile-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-values-by-profile-key?connectionId=$CONNECTION_ID&profileKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-values-by-profile-key?${params}`, {
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
| `profileKey` | string | yes | Agilit-e keyword profile key. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Optional sort expression supported by the Agilit-e endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /keywords/getValuesByProfileKey` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyword-values-by-profile-key.md) for the provider-specific parameters and requirements.

