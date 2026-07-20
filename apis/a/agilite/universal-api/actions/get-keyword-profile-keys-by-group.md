# Agilite: Get Keyword Profile Keys By Group

Retrieves keyword profile keys from Agilite by group.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-profile-keys-by-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-profile-keys-by-group?connectionId=$CONNECTION_ID&groupName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-profile-keys-by-group?${params}`, {
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
| `groupName` | string | yes | Agilit-e keyword group name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Optional sort expression supported by the Agilit-e endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "profileKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `profileKey` | string | Agilit-e keyword profile key. |

## Native endpoint

Through the native Agilite API, this operation is `GET /keywords/getProfileKeysByGroup` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyword-profile-keys-by-group.md) for the provider-specific parameters and requirements.

