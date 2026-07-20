# Moodo & Moodo AIR: Native API Reference

A consolidated summary of Moodo & Moodo AIR's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://rest.moodo.co
- **OpenAPI specification:** https://rest.moodo.co/api.yaml
- **API base URL:** `https://rest.moodo.co/api`

## Authentication

### Access Token

Use a Moodo access token and send it in the required `token` request header.

### Credentials

- **Access Token:** `token` · required · Your Moodo access token. The runtime sends this value in the `token` request header.

Send these headers with each API request:

```http
token: <token>
```

[Official authentication documentation](https://rest.moodo.co)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Terms And Conditions](actions/accept-terms-and-conditions.md) | `POST /terms_and_conditions` | [docs](https://rest.moodo.co/#/texts/accept_terms_and_conditions) |
| [Apply Favorite](actions/apply-favorite.md) | `PATCH /favorites` | [docs](https://rest.moodo.co/#/favorites/apply_favorite) |
| [Check Terms Acceptance](actions/check-terms-acceptance.md) | `PATCH /terms_and_conditions` | [docs](https://rest.moodo.co/#/texts/check_terms_and_conditions) |
| [Create Favorite](actions/create-favorite.md) | `POST /favorites` | [docs](https://rest.moodo.co/#/favorites/create_favorite) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://rest.moodo.co/#/schedules/create_schedule) |
| [Delete Favorite](actions/delete-favorite.md) | `DELETE /favorites/:id` | [docs](https://rest.moodo.co/#/favorites/delete_favorite) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedules/:id` | [docs](https://rest.moodo.co/#/schedules/delete_schedule) |
| [Disable Interval](actions/disable-interval.md) | `DELETE /interval/:device_key` | [docs](https://rest.moodo.co/#/interval/interval_disable) |
| [Disable Shuffle](actions/disable-shuffle.md) | `DELETE /shuffle/:device_key` | [docs](https://rest.moodo.co/#/shuffle/shuffle_disable) |
| [Enable Interval](actions/enable-interval.md) | `POST /interval/:device_key` | [docs](https://rest.moodo.co/#/interval/interval_enable) |
| [Enable Shuffle](actions/enable-shuffle.md) | `POST /shuffle/:device_key` | [docs](https://rest.moodo.co/#/shuffle/shuffle_enable) |
| [Get About Text](actions/get-about-text.md) | `GET /about` | [docs](https://rest.moodo.co/#/texts/get_about) |
| [Get Box](actions/get-box.md) | `GET /boxes/:device_key` | [docs](https://rest.moodo.co/#/boxes/get_box) |
| [Get FAQ](actions/get-faq.md) | `GET /faq` | [docs](https://rest.moodo.co/#/texts/get_faq) |
| [Get Interval Types](actions/get-interval-types.md) | `GET /interval` | [docs](https://rest.moodo.co/#/interval/get_interval_types) |
| [Get Privacy Policy](actions/get-privacy-policy.md) | `GET /privacy_policy` | [docs](https://rest.moodo.co/#/texts/get_privacy_policy) |
| [Get Terms And Conditions](actions/get-terms-and-conditions.md) | `GET /terms_and_conditions` | [docs](https://rest.moodo.co/#/texts/get_terms_and_conditions) |
| [List Box Favorites](actions/list-box-favorites.md) | `GET /favorites/:filter_my_favorites/:device_key` | [docs](https://rest.moodo.co/#/favorites/get_box_favorites) |
| [List Boxes](actions/list-boxes.md) | `GET /boxes` | [docs](https://rest.moodo.co/#/boxes/get_boxes) |
| [List Favorites](actions/list-favorites.md) | `GET /favorites` | [docs](https://rest.moodo.co/#/favorites/get_all_favorites) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://rest.moodo.co/#/schedules/get_schedules) |
| [Login](actions/login.md) | `POST /login` | [docs](https://rest.moodo.co/#/auth/login) |
| [Logout](actions/logout.md) | `POST /logout` | [docs](https://rest.moodo.co/#/auth/logout) |
| [Power Off Box](actions/power-off-box.md) | `DELETE /boxes/:device_key` | [docs](https://rest.moodo.co/#/boxes/power_off_box) |
| [Power On Box](actions/power-on-box.md) | `POST /boxes/:device_key` | [docs](https://rest.moodo.co/#/boxes/power_on_box) |
| [Register Box Serial](actions/register-box-serial.md) | `PATCH /boxes` | [docs](https://rest.moodo.co/#/boxes/register_box_serial) |
| [Rename Box](actions/rename-box.md) | `PUT /boxes/:device_key` | [docs](https://rest.moodo.co/#/boxes/name_box) |
| [Search Box Favorites](actions/search-box-favorites.md) | `GET /favorites/:filter_my_favorites/:device_key/:search_favorite_title` | [docs](https://rest.moodo.co/#/favorites/search_box_favorites) |
| [Set Box Intensity](actions/set-box-intensity.md) | `POST /intensity/:device_key` | [docs](https://rest.moodo.co/#/intensity/set_fan_volume) |
| [Set Up Box Wi-Fi](actions/setup-box-wifi.md) | `PATCH /boxes/:device_key` | [docs](https://rest.moodo.co/#/boxes/setup_wifi) |
| [Sign Up](actions/sign-up.md) | `POST /signup` | [docs](https://rest.moodo.co/#/auth/signup) |
| [Switch Box Mode](actions/switch-box-mode.md) | `POST /mode/:device_key` | [docs](https://rest.moodo.co/#/mode/switch_box_mode) |
| [Update Box](actions/update-box.md) | `POST /boxes` | [docs](https://rest.moodo.co/#/boxes/set_box) |
| [Update Box Fan Speeds](actions/update-box-fan-speeds.md) | `PUT /boxes` | [docs](https://rest.moodo.co/#/boxes/set_fan_speeds) |
| [Update Favorite](actions/update-favorite.md) | `PUT /favorites/:id` | [docs](https://rest.moodo.co/#/favorites/update_favorite) |
| [Update Schedule](actions/update-schedule.md) | `PUT /schedules/:id` | [docs](https://rest.moodo.co/#/schedules/update_schedule) |
| [Update Schedule Active State](actions/update-schedule-active-state.md) | `PATCH /schedules/:id` | [docs](https://rest.moodo.co/#/schedules/schedule_active_state) |
