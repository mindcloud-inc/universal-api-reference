# Create Testimonial with Senja

Creates a testimonial in your Senja project.

## Endpoint

- **Method:** `POST`
- **Path:** `/testimonials`
- **Base URL:** `https://api.senja.io/v1`
- **Official documentation:** [Create Testimonial](https://support.senja.io/articles/rest-api-wbnz4#create-a-testimonial)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_company` | body | `string` | no | The company name for the testimonial author. |
| `customer_email` | body | `string` | no | The email address of the testimonial author. |
| `customer_name` | body | `string` | yes | The name of the testimonial author. |
| `customer_tagline` | body | `string` | no | The job title or role for the testimonial author. |
| `customer_url` | body | `string` | no | A link associated with the testimonial author. |
| `image_url` | body | `string` | no | The image URL for the testimonial author. |
| `rating` | body | `number` | no | The testimonial rating. |
| `text` | body | `string` | no | The testimonial text. |
| `type` | body | `string` | no | The testimonial type. |
| `video_url` | body | `string` | no | The testimonial video URL. |
