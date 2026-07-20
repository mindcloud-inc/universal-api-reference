# <img src="https://images.mindcloud.co/apps/icons/payhip_1773343520843.png" alt="Payhip logo" width="28" height="28"> Payhip: Universal API

Manage Payhip coupons and license keys

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/payhip/latest
- **Category:** Commerce
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://payhip.com
- **Vendor API docs:** https://payhip.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Coupons](actions/list-coupons.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/list-coupons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a new coupon in Payhip. |
| [Get Coupon](actions/get-coupon.md) | GET | Retrieves a coupon from Payhip by ID. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves a paginated list of coupons from Payhip. |

### License Key

| Action | Method | Description |
| --- | --- | --- |
| [Decrease License Usage](actions/decrease-license-usage.md) | PUT | Decreases a Payhip license key usage count. |
| [Disable License Key](actions/disable-license-key.md) | PUT | Disables an existing license key in Payhip. |
| [Enable License Key](actions/enable-license-key.md) | PUT | Enables an existing license key in Payhip. |
| [Increase License Usage](actions/increase-license-usage.md) | PUT | Increases a Payhip license key usage count. |
| [Verify License Key](actions/verify-license-key.md) | GET | Verifies a Payhip license key and returns its details. |

