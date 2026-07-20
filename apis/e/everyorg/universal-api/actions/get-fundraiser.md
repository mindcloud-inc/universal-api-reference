# Every.org: Get Fundraiser

Retrieves details about a fundraiser from Every.org.

```
GET https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-fundraiser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Every.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-fundraiser?connectionId=$CONNECTION_ID&nonprofitIdentifier=string&fundraiserIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nonprofitIdentifier": "string",
  "fundraiserIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-fundraiser?${params}`, {
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
| `nonprofitIdentifier` | string | yes | A nonprofit slug, EIN, nonprofit ID, or special-fundraiser for multi-nonprofit fundraisers. |
| `fundraiserIdentifier` | string | yes | Fundraiser slug or identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fundraiser": {
        "active": true,
        "coverImageCloudinaryId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "creatorNonprofitId": "string",
        "creatorUserId": "string",
        "description": "string",
        "entityName": "Ava Chen",
        "goalAmount": "string",
        "goalCurrency": "string",
        "id": "string",
        "metadata": {
          "donationThankYouMessage": "string"
        },
        "nonprofitId": "string",
        "raisedData": {
          "currency": "string",
          "donations": 1,
          "goalAmount": "string",
          "goalType": "string",
          "raised": "string",
          "raisedMatches": "string",
          "raisedMonthly": "string",
          "raisedOffline": "string",
          "supporters": 1
        },
        "slug": "string",
        "title": "string",
        "type": "string"
      },
      "nonprofits": [
        {
          "archived": true,
          "causeCategory": "string",
          "countryCode": "string",
          "coverImageCloudinaryId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "descriptionLong": "string",
          "disbursementType": "string",
          "displayType": "string",
          "donationsEnabled": true,
          "donationThankYouMessage": "string",
          "eligibleDonationRecipientNonprofitIds": [
            "string"
          ],
          "entityName": "Ava Chen",
          "facebookHandle": "string",
          "hasAdmin": true,
          "hasDirectAdmin": true,
          "hideFromSearch": true,
          "holdDisbursements": true,
          "id": "string",
          "instagramHandle": "string",
          "isCaliforniaTaxBoardDisbursable": true,
          "likesInfo": {
            "count": 1,
            "hasLoggedInUserLiked": true
          },
          "linkedInHandle": "https://example.com",
          "logoCloudinaryId": "string",
          "metadata": {
            "customDonationAmounts": [
              1
            ],
            "customMonthlyDescription": "string",
            "focusArea": "string",
            "mailingListCheckboxText": "string",
            "optInCheckbox": true
          },
          "name": "Ava Chen",
          "pc": true,
          "primarySlug": "string",
          "supporterInfo": {
            "loggedInUserSupported": true,
            "numSupporters": 1
          },
          "tags": [
            "string"
          ],
          "twitterHandle": "string",
          "type": "string",
          "websiteUrl": "https://example.com"
        }
      ],
      "tags": [
        {
          "active": true,
          "causeCategory": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "entityName": "Ava Chen",
          "id": "string",
          "likesCount": 1,
          "showInFilters": true,
          "showInProfileEdit": true,
          "tagImageCloudinaryId": "string",
          "tagName": "Ava Chen",
          "title": "string"
        }
      ],
      "users": [
        {
          "entityName": "Ava Chen",
          "firstName": "Ava",
          "followedByCurrentUserStatus": "string",
          "id": "string",
          "isPrivate": true,
          "lastName": "Chen",
          "username": "Ava Chen",
          "verifiedStatus": "string"
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
| `fundraiser.active` | boolean |  |
| `fundraiser.coverImageCloudinaryId` | string |  |
| `fundraiser.createdAt` | date |  |
| `fundraiser.creatorNonprofitId` | string |  |
| `fundraiser.creatorUserId` | string |  |
| `fundraiser.description` | string |  |
| `fundraiser.entityName` | string |  |
| `fundraiser.goalAmount` | string |  |
| `fundraiser.goalCurrency` | string |  |
| `fundraiser.id` | string |  |
| `fundraiser.metadata.donationThankYouMessage` | string |  |
| `fundraiser.nonprofitId` | string |  |
| `fundraiser.raisedData.currency` | string |  |
| `fundraiser.raisedData.donations` | number |  |
| `fundraiser.raisedData.goalAmount` | string |  |
| `fundraiser.raisedData.goalType` | string |  |
| `fundraiser.raisedData.raised` | string |  |
| `fundraiser.raisedData.raisedMatches` | string |  |
| `fundraiser.raisedData.raisedMonthly` | string |  |
| `fundraiser.raisedData.raisedOffline` | string |  |
| `fundraiser.raisedData.supporters` | number |  |
| `fundraiser.slug` | string |  |
| `fundraiser.title` | string |  |
| `fundraiser.type` | string |  |
| `nonprofits[].archived` | boolean |  |
| `nonprofits[].causeCategory` | string |  |
| `nonprofits[].countryCode` | string |  |
| `nonprofits[].coverImageCloudinaryId` | string |  |
| `nonprofits[].createdAt` | date |  |
| `nonprofits[].description` | string |  |
| `nonprofits[].descriptionLong` | string |  |
| `nonprofits[].disbursementType` | string |  |
| `nonprofits[].displayType` | string |  |
| `nonprofits[].donationsEnabled` | boolean |  |
| `nonprofits[].donationThankYouMessage` | string |  |
| `nonprofits[].eligibleDonationRecipientNonprofitIds[]` | string |  |
| `nonprofits[].entityName` | string |  |
| `nonprofits[].facebookHandle` | string |  |
| `nonprofits[].hasAdmin` | boolean |  |
| `nonprofits[].hasDirectAdmin` | boolean |  |
| `nonprofits[].hideFromSearch` | boolean |  |
| `nonprofits[].holdDisbursements` | boolean |  |
| `nonprofits[].id` | string |  |
| `nonprofits[].instagramHandle` | string |  |
| `nonprofits[].isCaliforniaTaxBoardDisbursable` | boolean |  |
| `nonprofits[].likesInfo.count` | number |  |
| `nonprofits[].likesInfo.hasLoggedInUserLiked` | boolean |  |
| `nonprofits[].linkedInHandle` | string |  |
| `nonprofits[].logoCloudinaryId` | string |  |
| `nonprofits[].metadata.customDonationAmounts[]` | number |  |
| `nonprofits[].metadata.customMonthlyDescription` | string |  |
| `nonprofits[].metadata.focusArea` | string |  |
| `nonprofits[].metadata.mailingListCheckboxText` | string |  |
| `nonprofits[].metadata.optInCheckbox` | boolean |  |
| `nonprofits[].name` | string |  |
| `nonprofits[].pc` | boolean |  |
| `nonprofits[].primarySlug` | string |  |
| `nonprofits[].supporterInfo.loggedInUserSupported` | boolean |  |
| `nonprofits[].supporterInfo.numSupporters` | number |  |
| `nonprofits[].tags[]` | string |  |
| `nonprofits[].twitterHandle` | string |  |
| `nonprofits[].type` | string |  |
| `nonprofits[].websiteUrl` | string |  |
| `tags[].active` | boolean |  |
| `tags[].causeCategory` | string |  |
| `tags[].createdAt` | date |  |
| `tags[].entityName` | string |  |
| `tags[].id` | string |  |
| `tags[].likesCount` | number |  |
| `tags[].showInFilters` | boolean |  |
| `tags[].showInProfileEdit` | boolean |  |
| `tags[].tagImageCloudinaryId` | string |  |
| `tags[].tagName` | string |  |
| `tags[].title` | string |  |
| `users[].entityName` | string |  |
| `users[].firstName` | string |  |
| `users[].followedByCurrentUserStatus` | string |  |
| `users[].id` | string |  |
| `users[].isPrivate` | boolean |  |
| `users[].lastName` | string |  |
| `users[].username` | string |  |
| `users[].verifiedStatus` | string |  |

## Native endpoint

Through the native Every.org API, this operation is `GET /nonprofit/:nonprofitIdentifier/fundraiser/:fundraiserIdentifier` (base URL `https://partners.every.org/v0.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fundraiser.md) for the provider-specific parameters and requirements.

