# SurveyMethods: List Master Opt-Out Emails



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-master-opt-out-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-master-opt-out-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-master-opt-out-emails?${params}`, {
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
      "email_list": [
        {
          "email": "ava@example.com"
        }
      ],
      "rowcount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email_list` | array<object> |  |
| `email_list[].email` | string |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/emaillists/masteroptoutlist/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-master-opt-out-emails.md) for the provider-specific parameters and requirements.

