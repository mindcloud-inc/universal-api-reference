# Apollo Universal API Examples

These examples use the MindCloud API key and Apollo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile Info

Retrieves the authorized user profile from Apollo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "teamId": "string",
      "title": {}
    }
  ],
  "meta": {}
}
```

See the full [Get User Profile Info action reference](actions/get-user-profile-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apolloio/latest/actions/get-user-profile-info).

## Bulk Create Accounts

Creates multiple new accounts in Apollo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accounts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-accounts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accounts[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAccounts": [
        {
          "accountStageId": "string",
          "city": "string",
          "country": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "crmOwnerId": {},
          "crmRecordUrl": {},
          "domain": "string",
          "existenceLevel": "string",
          "facebookUrl": {},
          "hubspotId": {},
          "id": "string",
          "intentStrength": {},
          "linkedinUrl": {},
          "modality": "string",
          "name": "Ava Chen",
          "organizationHeadcountSixMonthGrowth": {},
          "organizationHeadcountTwelveMonthGrowth": {},
          "organizationHeadcountTwentyFourMonthGrowth": {},
          "organizationId": "string",
          "originalSource": "string",
          "ownerId": "string",
          "parentAccountId": {},
          "phone": {},
          "phoneStatus": "string",
          "postalCode": "string",
          "rawAddress": "string",
          "salesforceId": {},
          "showIntent": true,
          "source": "string",
          "sourceDisplayName": "Ava Chen",
          "state": "string",
          "streetAddress": "string",
          "suggestedFromRuleEngineConfigId": {},
          "teamId": "string",
          "twitterUrl": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Accounts action reference](actions/bulk-create-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apolloio/latest/actions/bulk-create-accounts).
