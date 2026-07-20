# Post Content with RecurPost

Creates a social post in RecurPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/post_content`
- **Base URL:** `https://social.recurpost.com`
- **Official documentation:** [Post Content](https://developers.recurpost.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bs_message` | body | `string` | no | — |
| `fb_first_comment` | body | `string` | no | — |
| `fb_message` | body | `string` | no | — |
| `fb_post_type` | body | `string` | no | — |
| `first_comment` | body | `string` | no | — |
| `gbp_cta` | body | `string` | no | — |
| `gbp_cta_url` | body | `string` | no | — |
| `gbp_offer_coupon_code` | body | `string` | no | — |
| `gbp_offer_end_date` | body | `string` | no | — |
| `gbp_offer_start_date` | body | `string` | no | — |
| `gbp_offer_terms` | body | `string` | no | — |
| `gbp_offer_title` | body | `string` | no | — |
| `gbp_redeem_offer_link` | body | `string` | no | — |
| `gmb_message` | body | `string` | no | — |
| `host_images_on_recurpost` | body | `boolean` | no | — |
| `id` | body | `string` | yes | Social account ID from List Social Accounts. |
| `image_url[]` | body | `array<string>` | no | — |
| `in_first_comment` | body | `string` | no | — |
| `in_message` | body | `string` | no | — |
| `in_post_type` | body | `string` | no | — |
| `in_reel_share_in_feed` | body | `string` | no | — |
| `ln_document` | body | `string` | no | — |
| `ln_document_title` | body | `string` | no | — |
| `ln_first_comment` | body | `string` | no | — |
| `ln_message` | body | `string` | no | — |
| `message` | body | `string` | yes | Message or content for the post. |
| `pi_message` | body | `string` | no | — |
| `pi_title` | body | `string` | no | — |
| `schedule_date_time` | body | `string` | no | — |
| `th_message` | body | `string` | no | — |
| `tk_allow_comments` | body | `string` | no | — |
| `tk_allow_duet` | body | `string` | no | — |
| `tk_allow_stitches` | body | `string` | no | — |
| `tk_message` | body | `string` | no | — |
| `tk_privacy_status` | body | `string` | no | — |
| `tw_message` | body | `string` | no | — |
| `url` | body | `string` | no | — |
| `video_url` | body | `string` | no | — |
| `yt_category` | body | `string` | no | — |
| `yt_message` | body | `string` | no | — |
| `yt_privacy_status` | body | `string` | no | — |
| `yt_thumb` | body | `string` | no | — |
| `yt_title` | body | `string` | no | — |
| `yt_user_tags` | body | `string` | no | — |
| `yt_video_made_for_kids` | body | `string` | no | — |
