# Zoho WorkDrive: Get All Labels of the User

Retrieves labels for a Zoho WorkDrive user.

```
GET https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-all-labels-of-the-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho WorkDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-all-labels-of-the-user?connectionId=$CONNECTION_ID&teamMemberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamMemberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-all-labels-of-the-user?${params}`, {
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
| `teamMemberId` | string | yes | The team member ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Provider resource attributes. |
| `id` | string | Resource ID. |
| `links` | object | Provider self and related links. |
| `relationships` | object | Provider relationship links. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Zoho WorkDrive API, this operation is `GET /api/v1/users/:teamMemberId/labels` (base URL `{{credentials.accessTokenRequest.api_domain}}/workdrive`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-labels-of-the-user.md) for the provider-specific parameters and requirements.

