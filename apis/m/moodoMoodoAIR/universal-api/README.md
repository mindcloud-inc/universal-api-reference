# <img src="https://images.mindcloud.co/apps/icons/moodo-moodo-air_1776369448562.png" alt="Moodo & Moodo AIR logo" width="28" height="28"> Moodo & Moodo AIR: Universal API

Control and manage Moodo and Moodo AIR devices, favorites, schedules, interval/shuffle modes, and account text resources via the Moodo RESTful API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moodoMoodoAIR/latest
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moodo.co
- **Vendor API docs:** https://rest.moodo.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Boxes](actions/list-boxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/list-boxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a new schedule for a Moodo box. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from Moodo & Moodo AIR. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Moodo & Moodo AIR. |
| [Update Schedule](actions/update-schedule.md) | PUT | Updates an existing schedule for a Moodo box. |
| [Update Schedule Active State](actions/update-schedule-active-state.md) | PUT | Updates a schedule's active state in Moodo. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Accept Terms And Conditions](actions/accept-terms-and-conditions.md) | PUT | Accepts the Terms and Conditions in Moodo. |
| [Apply Favorite](actions/apply-favorite.md) | PUT | Applies a favorite to a Moodo box. |
| [Check Terms Acceptance](actions/check-terms-acceptance.md) | PUT | Checks whether Terms and Conditions were previously accepted. |
| [Create Favorite](actions/create-favorite.md) | POST | Creates a new favorite in Moodo & Moodo AIR. |
| [Delete Favorite](actions/delete-favorite.md) | DELETE | Deletes an existing favorite from Moodo & Moodo AIR. |
| [Disable Interval](actions/disable-interval.md) | DELETE | Disables interval mode on a Moodo box. |
| [Disable Shuffle](actions/disable-shuffle.md) | DELETE | Disables shuffle mode on a Moodo box. |
| [Enable Interval](actions/enable-interval.md) | PUT | Enables interval mode on a Moodo box. |
| [Enable Shuffle](actions/enable-shuffle.md) | PUT | Enables shuffle mode on a Moodo box. |
| [Get About Text](actions/get-about-text.md) | GET | Retrieves the about page text from Moodo. |
| [Get Box](actions/get-box.md) | GET | Retrieves a Moodo box by device key. |
| [Get FAQ](actions/get-faq.md) | GET | Retrieves the FAQ text from Moodo. |
| [Get Interval Types](actions/get-interval-types.md) | GET | Retrieves interval types from Moodo & Moodo AIR. |
| [Get Privacy Policy](actions/get-privacy-policy.md) | GET | Retrieves the privacy policy text from Moodo. |
| [Get Terms And Conditions](actions/get-terms-and-conditions.md) | GET | Retrieves the Terms and Conditions text from Moodo. |
| [List Box Favorites](actions/list-box-favorites.md) | GET | Retrieves favorites for a Moodo box configuration. |
| [List Boxes](actions/list-boxes.md) | GET | Retrieves Moodo boxes available to the current user. |
| [List Favorites](actions/list-favorites.md) | GET | Retrieves available favorites from Moodo & Moodo AIR. |
| [Login](actions/login.md) | POST | Authenticates a Moodo user and returns a token. |
| [Logout](actions/logout.md) | DELETE | Signs the current user out of Moodo. |
| [Power Off Box](actions/power-off-box.md) | DELETE | Powers off a Moodo box in Moodo. |
| [Power On Box](actions/power-on-box.md) | PUT | Powers on a Moodo box in Moodo. |
| [Register Box Serial](actions/register-box-serial.md) | PUT | Registers a Moodo box serial to the current account. |
| [Rename Box](actions/rename-box.md) | PUT | Updates a Moodo box's name in Moodo. |
| [Search Box Favorites](actions/search-box-favorites.md) | GET | Finds favorites for a Moodo box by title. |
| [Set Box Intensity](actions/set-box-intensity.md) | PUT | Updates a Moodo box's main fan intensity. |
| [Set Up Box Wi-Fi](actions/setup-box-wifi.md) | PUT | Updates a Moodo box's Wi-Fi credentials. |
| [Sign Up](actions/sign-up.md) | POST | Creates a Moodo user and returns a token. |
| [Switch Box Mode](actions/switch-box-mode.md) | PUT | Updates a Moodo box's mode between diffuser and purifier. |
| [Update Box](actions/update-box.md) | PUT | Updates a Moodo box's fan and power state. |
| [Update Box Fan Speeds](actions/update-box-fan-speeds.md) | PUT | Updates a Moodo box's individual fan speeds. |
| [Update Favorite](actions/update-favorite.md) | PUT | Updates an existing favorite in Moodo & Moodo AIR. |

