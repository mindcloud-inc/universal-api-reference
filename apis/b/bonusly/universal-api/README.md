# <img src="https://images.mindcloud.co/apps/icons/bonusly_1782741409254.png" alt="Bonusly logo" width="28" height="28"> Bonusly: Universal API

Bonusly is an employee recognition and rewards platform for peer-to-peer recognition, incentives, and engagement.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bonusly/latest
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bonusly.com/
- **Vendor API docs:** https://docs.bonus.ly/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Me](actions/me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Achievement

| Action | Method | Description |
| --- | --- | --- |
| [List Achievements](actions/list-achievements.md) | GET | Retrieves achievements from Bonusly. |
| [List User Achievements](actions/list-user-achievements.md) | GET | Retrieves achievements for a Bonusly user. |

### Analytics Leaderboard

| Action | Method | Description |
| --- | --- | --- |
| [Leaderboards](actions/leaderboards.md) | GET | Retrieves leaderboard analytics from Bonusly. |

### Analytics Trend

| Action | Method | Description |
| --- | --- | --- |
| [Trends](actions/trends.md) | GET | Retrieves trend analytics from Bonusly. |

### Analytics Word

| Action | Method | Description |
| --- | --- | --- |
| [Get Popular Words](actions/get-popular-words.md) | GET | Retrieves popular words analytics from Bonusly. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from Bonusly. |

### Bonus

| Action | Method | Description |
| --- | --- | --- |
| [Create Bonus](actions/create-bonus.md) | POST | Creates a new bonus in Bonusly. |
| [List Bonuses](actions/list-bonuses.md) | GET | Retrieves bonuses from Bonusly. |
| [List User Bonuses](actions/list-user-bonuses.md) | GET | Retrieves bonuses for a Bonusly user. |
| [Retrieve Bonus](actions/retrieve-bonus.md) | GET | Retrieves a bonus from Bonusly. |

### Bonus Feed

| Action | Method | Description |
| --- | --- | --- |
| [XML List Bonuses](actions/xml-list-bonuses.md) | GET | Retrieves bonuses from Bonusly as an Atom feed. |

### Custom Reward Redemption

| Action | Method | Description |
| --- | --- | --- |
| [Approve Custom Reward Redemptions](actions/approve-custom-reward-redemptions.md) | PUT | Approves custom reward redemptions in Bonusly. |
| [Fulfill Custom Reward Redemptions](actions/fulfill-custom-reward-redemptions.md) | PUT | Fulfills custom reward redemptions in Bonusly. |
| [List Custom Rewards Redemptions](actions/list-custom-rewards-redemptions.md) | GET | Retrieves custom reward redemptions from Bonusly. |

### Participation Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Participation Rates](actions/get-participation-rates.md) | GET | Retrieves participation rates from Bonusly. |

### Recognition Add-on

| Action | Method | Description |
| --- | --- | --- |
| [Get Recognition Add-ons](actions/get-recognition-add-ons.md) | GET | Retrieves recognition add-on analytics from Bonusly. |

### Recognition Hashtag

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Value Hashtags Received](actions/get-company-value-hashtags-received.md) | GET | Retrieves company value hashtag analytics from Bonusly. |
| [Get Hashtags Received](actions/get-hashtags-received.md) | GET | Retrieves received hashtag analytics from Bonusly. |

### Recognition Points

| Action | Method | Description |
| --- | --- | --- |
| [Get Points Received](actions/get-points-received.md) | GET | Retrieves received points analytics from Bonusly. |

### Recognition Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Recognition Rates](actions/get-recognition-rates.md) | GET | Retrieves recognition rates from Bonusly. |

### Recognition Received

| Action | Method | Description |
| --- | --- | --- |
| [Get Recognition Received](actions/get-recognition-received.md) | GET | Retrieves received recognition analytics from Bonusly. |

### Recognition User Count

| Action | Method | Description |
| --- | --- | --- |
| [Get User Count](actions/get-user-count.md) | GET | Retrieves recognition user counts from Bonusly. |

### Redemption

| Action | Method | Description |
| --- | --- | --- |
| [Create Redemption](actions/create-redemption.md) | POST | Creates a redemption for a Bonusly user. |
| [List Redemptions](actions/list-redemptions.md) | GET | Retrieves redemptions from Bonusly. |
| [List User Redemptions](actions/list-user-redemptions.md) | GET | Retrieves redemptions for a Bonusly user. |
| [Retrieve Redemption](actions/retrieve-redemption.md) | GET | Retrieves a redemption from Bonusly. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [List Rewards](actions/list-rewards.md) | GET | Retrieves rewards from Bonusly. |
| [Retrieve Reward](actions/retrieve-reward.md) | GET | Retrieves a reward from Bonusly. |

### Scim Schema

| Action | Method | Description |
| --- | --- | --- |
| [List SCIM Schemas](actions/list-scim-schemas.md) | GET | Retrieves SCIM schemas from Bonusly. |

### Scim Service Provider Config

| Action | Method | Description |
| --- | --- | --- |
| [Get SCIM Metadata](actions/get-scim-metadata.md) | GET | Retrieves SCIM service provider metadata from Bonusly. |

### Scim User

| Action | Method | Description |
| --- | --- | --- |
| [SCIM Activate Or Deactivate User](actions/scim-activate-or-deactivate-user.md) | DELETE | Activates or deactivates a SCIM user in Bonusly. |
| [SCIM Create User](actions/scim-create-user.md) | POST | Creates a new SCIM user in Bonusly. |
| [SCIM List Users](actions/scim-list-users.md) | GET | Retrieves SCIM users from Bonusly. |
| [SCIM Retrieve User](actions/scim-retrieve-user.md) | GET | Retrieves a SCIM user from Bonusly. |
| [SCIM Update User](actions/scim-update-user.md) | PUT | Updates an existing SCIM user in Bonusly. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Admin Create User](actions/admin-create-user.md) | POST | Creates a new user in Bonusly. |
| [Admin Deactivate User](actions/admin-deactivate-user.md) | DELETE | Deactivates an existing user in Bonusly. |
| [Admin Update User](actions/admin-update-user.md) | PUT | Updates an existing user in Bonusly. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Bonusly. |
| [Me](actions/me.md) | GET | Retrieves the authenticated user from Bonusly. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from Bonusly. |
| [Search Users](actions/search-users.md) | GET | Finds users in Bonusly by search term. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Bonusly. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Bonusly. |
| [Remove Webhook](actions/remove-webhook.md) | DELETE | Deletes an existing webhook from Bonusly. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Bonusly. |

