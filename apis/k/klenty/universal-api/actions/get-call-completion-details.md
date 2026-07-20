# Klenty: Get Call Completion Details

Retrieves call completion details from Klenty.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-call-completion-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-call-completion-details?connectionId=$CONNECTION_ID&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-call-completion-details?${params}`, {
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
| `endDate` | string | yes | End date for the call report window. Use yyyy-mm-dd. |
| `page` | string | no | Page number for paginating call completion results. Default: `0`. |
| `startDate` | string | yes | Start date for the call report window. Use yyyy-mm-dd. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "code": "string",
          "errorMessage": "string"
        }
      ],
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[].code` | string |  |
| `errors[].errorMessage` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Klenty API, this operation is `GET /calls` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-completion-details.md) for the provider-specific parameters and requirements.

