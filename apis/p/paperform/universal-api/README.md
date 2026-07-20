# <img src="https://images.mindcloud.co/apps/icons/paperform_1773164887136.png" alt="Paperform logo" width="28" height="28"> Paperform: Universal API

Create forms, collect submissions, and manage bookings and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paperform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://paperform.co
- **Vendor API docs:** https://paperform.readme.io/reference/getting-started-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Coupon](actions/get-form-coupon.md) | GET | Retrieves a coupon from a Paperform form. |
| [List Form Coupons](actions/list-form-coupons.md) | GET | Retrieves coupons from a Paperform form. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Field](actions/get-form-field.md) | GET | Retrieves a field from a Paperform form. |
| [List Form Fields](actions/list-form-fields.md) | GET | Retrieves fields from a Paperform form. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Paperform. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Paperform. |

### Partial Submission

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Partial Submission](actions/get-form-partial-submission.md) | GET | Retrieves a partial submission from a Paperform form. |
| [Get Partial Submission](actions/get-partial-submission.md) | GET | Retrieves a partial submission from Paperform. |
| [List Form Partial Submissions](actions/list-form-partial-submissions.md) | GET | Retrieves partial submissions from a Paperform form. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Product](actions/get-form-product.md) | GET | Retrieves a product from a Paperform form. |
| [List Form Products](actions/list-form-products.md) | GET | Retrieves products from a Paperform form. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Submission](actions/get-form-submission.md) | GET | Retrieves a submission from a Paperform form. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a submission from Paperform. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves submissions from a Paperform form. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Form Webhooks](actions/list-form-webhooks.md) | GET | Retrieves webhooks from a Paperform form. |

