# <img src="https://images.mindcloud.co/apps/icons/idq-s-gvv-q-logos_1775149562791.jpeg" alt="Weberlo logo" width="28" height="28"> Weberlo: Universal API

Track attribution, analyze campaigns, and measure marketing performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weberlo/latest
- **Category:** Marketing
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weberlo.com/
- **Vendor API docs:** https://developers.weberlo.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Websites](actions/list-websites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-websites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Ad Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Ad Channel](actions/create-ad-channel.md) | POST | Creates an ad channel in Weberlo. |
| [Delete Ad Channel](actions/delete-ad-channel.md) | DELETE | Deletes an ad channel from Weberlo. |
| [Get Ad Channel](actions/get-ad-channel.md) | GET | Retrieves an ad channel from Weberlo. |
| [Update Ad Channel](actions/update-ad-channel.md) | PUT | Updates an ad channel in Weberlo. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Weberlo. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes an existing channel from Weberlo. |
| [List Channels](actions/list-channels.md) | GET | Retrieves a list of channels from Weberlo. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Submit Event](actions/create-form-submit-event.md) | POST | Creates a form submit event in Weberlo. |
| [Create Transaction Event](actions/create-transaction-event.md) | POST | Creates a transaction event in Weberlo. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Persons](actions/list-persons.md) | GET | Retrieves a list of persons from Weberlo. |
| [List Visitors](actions/list-visitors.md) | GET | Retrieves a list of visitors from Weberlo. |
| [Search Pages](actions/search-pages.md) | GET | Finds pages in Weberlo by search query. |

### Utm Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create UTM Channel](actions/create-utm-channel.md) | POST | Creates a UTM channel in Weberlo. |
| [Delete UTM Channel](actions/delete-utm-channel.md) | DELETE | Deletes a UTM channel from Weberlo. |
| [Get UTM Channel](actions/get-utm-channel.md) | GET | Retrieves a UTM channel from Weberlo. |
| [Update UTM Channel](actions/update-utm-channel.md) | PUT | Updates a UTM channel in Weberlo. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [List Websites](actions/list-websites.md) | GET | Retrieves a list of websites from Weberlo. |

