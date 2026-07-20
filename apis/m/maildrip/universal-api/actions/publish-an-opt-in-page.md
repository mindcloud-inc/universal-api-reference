# Maildrip: Publish an opt-in page



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/publish-an-opt-in-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/publish-an-opt-in-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/publish-an-opt-in-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | ID of the opt-in page to publish |
| `backgroundColor` | string | no | Background color for the page |
| `bannerColor` | string | no | Background color for the banner |
| `footerColor` | string | no | Background color for the footer |
| `heading` | string | no | Heading text for the page |
| `body` | string | no | Body text for the page |
| `facebook` | string | no | URL for social platform |
| `instagram` | string | no | URL of the social platform |
| `twitter` | string | no | URL for social platform |
| `linkedIn` | string | no | URL for social platform |
| `youtube` | string | no | URL for social platform |
| `tiktok` | string | no | URL for social platform |
| `buttonText` | string | no | Text for the button |
| `buttonBgColor` | string | no | Background color of the button |
| `buttonRedirectLink` | string | no | Redirect link for the button |
| `logo` | string | no | URL of page logo |
| `heroImage` | string | no | URL of page hero image |
| `templateId` | string | no | The template id |
| `businessMail` | string | no | Business mail of user |
| `phoneNumber` | string | no | Phone number of user |
| `formFields[]` | array<object> | no | Array of form fields (optional) Accepts multiple values as an array. |
| `contactGroups[]` | array<string> | no | Array of contact group IDs (optional) Accepts multiple values as an array. |
| `pageUrl` | string | no | The custom opt-in page url |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated opt-in page data |
| `message` | string | Confirmation message of successful publication |

## Native endpoint

Through the native Maildrip API, this operation is `PUT /api/v1/opt-in-pages/{pageId}/publish` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-an-opt-in-page.md) for the provider-specific parameters and requirements.

