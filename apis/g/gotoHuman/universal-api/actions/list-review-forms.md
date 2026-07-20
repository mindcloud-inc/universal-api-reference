# gotoHuman: List Review Forms

Retrieves review templates from gotoHuman.

```
GET https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/list-review-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gotoHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/list-review-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/list-review-forms?${params}`, {
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
      "forms": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forms` | array<object> | Review forms available in the gotoHuman workspace. |

## Native endpoint

Through the native gotoHuman API, this operation is `GET /fetchReviewForms` (base URL `https://api.gotohuman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-review-forms.md) for the provider-specific parameters and requirements.

