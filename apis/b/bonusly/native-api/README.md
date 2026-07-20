# Bonusly: Native API Reference

A consolidated summary of Bonusly's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://docs.bonus.ly/
- **API base URL:** `https://bonus.ly/api/v1`

## Authentication

### API Key

Bonusly uses personal API access tokens. The API reference also shows an access_token query parameter, but the official help guide recommends using the Authorization header with a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.bonus.ly/en/articles/1258685-connecting-to-the-bonusly-api)

## API conventions

Response data is read from `result`.

## Pagination

Use `limit` in the query string to set the page size (default 1; minimum 1). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Admin Create User](actions/admin-create-user.md) | `POST /users` | [docs](https://docs.bonus.ly/reference/admin-create-a-user) |
| [Admin Deactivate User](actions/admin-deactivate-user.md) | `DELETE /users/:id` | [docs](https://docs.bonus.ly/reference/admin-deactivate-a-user) |
| [Admin Update User](actions/admin-update-user.md) | `PUT /users/:id` | [docs](https://docs.bonus.ly/reference/admin-update-a-user) |
| [Approve Custom Reward Redemptions](actions/approve-custom-reward-redemptions.md) | `POST /custom_rewards_redemptions/approve` | [docs](https://docs.bonus.ly/reference/approve-custom-reward-redemptions) |
| [Create Bonus](actions/create-bonus.md) | `POST /bonuses` | [docs](https://docs.bonus.ly/reference/create-a-bonus) |
| [Create Redemption](actions/create-redemption.md) | `POST /users/:id/redemptions` | [docs](https://docs.bonus.ly/reference/create-a-redemption) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.bonus.ly/reference/create-webhook) |
| [Fulfill Custom Reward Redemptions](actions/fulfill-custom-reward-redemptions.md) | `POST /custom_rewards_redemptions/fulfill` | [docs](https://docs.bonus.ly/reference/fulfill-custom-reward-redemptions) |
| [Get Company Value Hashtags Received](actions/get-company-value-hashtags-received.md) | `GET /data_layer/recognition/hashtags_core_value` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-hashtags-core-value) |
| [Get Hashtags Received](actions/get-hashtags-received.md) | `GET /data_layer/recognition/hashtags_all` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-hashtags-all) |
| [Get Participation Rates](actions/get-participation-rates.md) | `GET /data_layer/participation` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-participation) |
| [Get Points Received](actions/get-points-received.md) | `GET /data_layer/recognition/points_received` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-points-received) |
| [Get Popular Words](actions/get-popular-words.md) | `GET /analytics/words` | [docs](https://docs.bonus.ly/reference/get_v1-analytics-words) |
| [Get Recognition Add-ons](actions/get-recognition-add-ons.md) | `GET /data_layer/recognition/addons` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-addons) |
| [Get Recognition Rates](actions/get-recognition-rates.md) | `GET /data_layer/recognition/rates` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-rates) |
| [Get Recognition Received](actions/get-recognition-received.md) | `GET /data_layer/recognition/bonuses_received` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-bonuses-received) |
| [Get SCIM Metadata](actions/get-scim-metadata.md) | `GET https://bonus.ly/api/scim11/ServiceProviderConfigs` | [docs](https://docs.bonus.ly/reference/get-metadata-about-the-bonusly-scim-api) |
| [Get User Count](actions/get-user-count.md) | `GET /data_layer/recognition/user_count` | [docs](https://docs.bonus.ly/reference/get_v1-data-layer-recognition-user-count) |
| [Leaderboards](actions/leaderboards.md) | `GET /analytics/leaderboards` | [docs](https://docs.bonus.ly/reference/leaderboards) |
| [List Achievements](actions/list-achievements.md) | `GET /achievements` | [docs](https://docs.bonus.ly/reference/list-achievements) |
| [List API Keys](actions/list-api-keys.md) | `GET /api_keys` | [docs](https://docs.bonus.ly/reference/list-api-keys) |
| [List Bonuses](actions/list-bonuses.md) | `GET /bonuses` | [docs](https://docs.bonus.ly/reference/list-bonuses) |
| [List Custom Rewards Redemptions](actions/list-custom-rewards-redemptions.md) | `GET /custom_rewards_redemptions` | [docs](https://docs.bonus.ly/reference/list-custom-rewards-redemptions) |
| [List Redemptions](actions/list-redemptions.md) | `GET /redemptions` | [docs](https://docs.bonus.ly/reference/list-redemptions) |
| [List Rewards](actions/list-rewards.md) | `GET /rewards` | [docs](https://docs.bonus.ly/reference/list-rewards) |
| [List SCIM Schemas](actions/list-scim-schemas.md) | `GET https://bonus.ly/api/scim11/Schemas` | [docs](https://docs.bonus.ly/reference/list-the-scim-schemas-supported-by-bonusly) |
| [List User Achievements](actions/list-user-achievements.md) | `GET /users/:id/achievements` | [docs](https://docs.bonus.ly/reference/achievements-1) |
| [List User Bonuses](actions/list-user-bonuses.md) | `GET /users/:id/bonuses` | [docs](https://docs.bonus.ly/reference/bonuses-1) |
| [List User Redemptions](actions/list-user-redemptions.md) | `GET /users/:id/redemptions` | [docs](https://docs.bonus.ly/reference/redemptions-1) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.bonus.ly/reference/list-users-1) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.bonus.ly/reference/list-webhooks) |
| [Me](actions/me.md) | `GET /users/me` | [docs](https://docs.bonus.ly/reference/me) |
| [Remove Webhook](actions/remove-webhook.md) | `DELETE /webhooks/:id` | [docs](https://docs.bonus.ly/reference/remove-a-webhook) |
| [Retrieve Bonus](actions/retrieve-bonus.md) | `GET /bonuses/:id` | [docs](https://docs.bonus.ly/reference/retrieve-a-bonus) |
| [Retrieve Redemption](actions/retrieve-redemption.md) | `GET /redemptions/:id` | [docs](https://docs.bonus.ly/reference/retrieve-a-redemption) |
| [Retrieve Reward](actions/retrieve-reward.md) | `GET /rewards/:id` | [docs](https://docs.bonus.ly/reference/retrieve-a-reward) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:id` | [docs](https://docs.bonus.ly/reference/retrieve-a-user-1) |
| [SCIM Activate Or Deactivate User](actions/scim-activate-or-deactivate-user.md) | `DELETE https://bonus.ly/api/scim11/Users/:id` | [docs](https://docs.bonus.ly/reference/activate-or-deactivate-a-user) |
| [SCIM Create User](actions/scim-create-user.md) | `POST https://bonus.ly/api/scim11/Users` | [docs](https://docs.bonus.ly/reference/create-a-user) |
| [SCIM List Users](actions/scim-list-users.md) | `GET https://bonus.ly/api/scim11/Users` | [docs](https://docs.bonus.ly/reference/list-users) |
| [SCIM Retrieve User](actions/scim-retrieve-user.md) | `GET https://bonus.ly/api/scim11/Users/:id` | [docs](https://docs.bonus.ly/reference/list-users) |
| [SCIM Update User](actions/scim-update-user.md) | `PUT https://bonus.ly/api/scim11/Users/:id` | [docs](https://docs.bonus.ly/reference/update-an-existing-user) |
| [Search Users](actions/search-users.md) | `GET /users/autocomplete` | [docs](https://docs.bonus.ly/reference/autocomplete) |
| [Trends](actions/trends.md) | `GET /analytics/trends` | [docs](https://docs.bonus.ly/reference/trends) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id` | [docs](https://docs.bonus.ly/reference/update-a-webhook) |
| [XML List Bonuses](actions/xml-list-bonuses.md) | `GET /bonuses.atom` | [docs](https://docs.bonus.ly/reference/xml-list-bonuses) |
