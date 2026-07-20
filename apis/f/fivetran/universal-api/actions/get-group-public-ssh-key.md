# Fivetran: Get Group Public SSH Key

Retrieves a group's public SSH key from Fivetran.

```
GET https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-group-public-ssh-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-group-public-ssh-key?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-group-public-ssh-key?${params}`, {
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
| `groupId` | string | yes | The unique identifier for the group within Fivetran. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "publicKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publicKey` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `GET /groups/[:groupId]/public-key` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-public-ssh-key.md) for the provider-specific parameters and requirements.

