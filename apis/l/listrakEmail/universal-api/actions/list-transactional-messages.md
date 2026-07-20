# Listrak Email: List Transactional Messages



```
GET https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/list-transactional-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listrak Email `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/list-transactional-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&listID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "listID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/list-transactional-messages?${params}`, {
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
| `listID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounceDomainAlias": "string",
      "bounceHandling": "string",
      "bounceUnsubscribeCount": 1,
      "createDate": "string",
      "enableBrowserLink": true,
      "enableDoubleOptIn": true,
      "enableDynamicContent": true,
      "enableGoogleAnalytics": true,
      "enableInternationalization": true,
      "enableListHygiene": true,
      "enableListrakAnalytics": true,
      "enableListRemovalHeader": true,
      "enableListRemovalLink": true,
      "enableSpamScorePersonalization": true,
      "enableToNamePersonalization": true,
      "enableUniversalEmailKeySetting": true,
      "folderId": 1,
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "ipPoolId": 1,
      "linkDomainAlias": "https://example.com",
      "listId": 1,
      "listName": "Ava Chen",
      "mediaDomainAlias": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceDomainAlias` | string |  |
| `bounceHandling` | string |  |
| `bounceUnsubscribeCount` | number |  |
| `createDate` | string |  |
| `enableBrowserLink` | boolean |  |
| `enableDoubleOptIn` | boolean |  |
| `enableDynamicContent` | boolean |  |
| `enableGoogleAnalytics` | boolean |  |
| `enableInternationalization` | boolean |  |
| `enableListHygiene` | boolean |  |
| `enableListrakAnalytics` | boolean |  |
| `enableListRemovalHeader` | boolean |  |
| `enableListRemovalLink` | boolean |  |
| `enableSpamScorePersonalization` | boolean |  |
| `enableToNamePersonalization` | boolean |  |
| `enableUniversalEmailKeySetting` | boolean |  |
| `folderId` | number |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `ipPoolId` | number |  |
| `linkDomainAlias` | string |  |
| `listId` | number |  |
| `listName` | string |  |
| `mediaDomainAlias` | string |  |

## Native endpoint

Through the native Listrak Email API, this operation is `GET /v1/List/:listID/TransactionalMessage` (base URL `https://api.listrak.com/email`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactional-messages.md) for the provider-specific parameters and requirements.

