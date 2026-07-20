# Socket: List Repository Labels

Retrieves repository labels configured in Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-repository-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-repository-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-repository-labels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": 1,
      "results": [
        {
          "hasLicensePolicy": true,
          "hasSecurityPolicy": true,
          "id": "string",
          "name": "Ava Chen",
          "repositoryIds": [
            "string"
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | number |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].hasLicensePolicy` | boolean | Whether the label has a license policy |
| `results[].hasSecurityPolicy` | boolean | Whether the label has a security policy |
| `results[].id` | string | The ID of the label |
| `results[].name` | string | The name of the label |
| `results[].repositoryIds` | array<string> |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/repos/labels` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-repository-labels.md) for the provider-specific parameters and requirements.

