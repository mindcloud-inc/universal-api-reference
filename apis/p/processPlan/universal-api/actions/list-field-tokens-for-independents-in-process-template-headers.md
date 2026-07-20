# Process Plan: List Field Tokens for Independents in Process Template Headers



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-field-tokens-for-independents-in-process-template-headers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-field-tokens-for-independents-in-process-template-headers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-field-tokens-for-independents-in-process-template-headers?${params}`, {
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
      "field_token_list": [
        {
          "display_text": "string",
          "field_token": "string",
          "is_advanced_token": true,
          "is_email_token": true,
          "is_html_token": true,
          "is_multi_row_field": true,
          "is_user_id_token": true
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
| `field_token_list[].display_text` | string |  |
| `field_token_list[].field_token` | string |  |
| `field_token_list[].is_advanced_token` | boolean |  |
| `field_token_list[].is_email_token` | boolean |  |
| `field_token_list[].is_html_token` | boolean |  |
| `field_token_list[].is_multi_row_field` | boolean |  |
| `field_token_list[].is_user_id_token` | boolean |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/independent/field_token/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-field-tokens-for-independents-in-process-template-headers.md) for the provider-specific parameters and requirements.

