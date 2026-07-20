# Scrapeless: Get Scraper Result

Retrieves a scraper result from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-scraper-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-scraper-result?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-scraper-result?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": {
        "bff_meta": "string",
        "data": {
          "abnormal_popup": "string",
          "account": {
            "adult_consent": "string",
            "birth_timestamp": "string",
            "default_address": {
              "address": "string",
              "city": "string",
              "district": "string",
              "latitude": "string",
              "longitude": "string",
              "region": "string",
              "state": "string",
              "town": "string",
              "zip_code": "string"
            },
            "is_new_user": "string",
            "user_id": "string"
          },
          "age_gate": {
            "kyc": "string"
          },
          "age_gate_control": "string",
          "alcohol_disclaimer": "string",
          "button_group": {
            "buy_with_voucher": "string"
          },
          "coin_info": {
            "coin_earn_items": [
              "string"
            ],
            "coin_earn_label": "string",
            "spend_cash_unit": 1
          },
          "deep_discount": "string",
          "design_control": {
            "disable_price_with_variation": true,
            "display_choice_customised_section": true,
            "display_direct_delivery": true,
            "display_on_time_delivery_guarantee": true,
            "enable_ksp_config": "string",
            "first_screen_revamp_abtest_group": "string",
            "is_support_fbs_enabled": true,
            "top_section_featured_video_ab_test_group": "string",
            "use_new_featured_video_revamp": "string",
            "use_new_revamp_first_screen": "string"
          },
          "designer_info": "string",
          "detail_level": 1,
          "display_sections": {
            "add_on_deal": "string",
            "bundle_deal": "string",
            "coin": "string",
            "exclusive_price_label": "string",
            "free_return": "string",
            "wholesale": "string"
          },
          "exclusive_price": "string",
          "exclusive_price_cta": "string",
          "flash_sale": "string",
          "flash_sale_preview": "string",
          "free_return": "string",
          "ineligible_ep": "string",
          "installment_drawer": "string",
          "item": {
            "add_on_deal_info": "string",
            "all_models_has_pre_order": true,
            "attributes": {
              "brand_id": "string",
              "brand_option": "string",
              "full_url": "https://example.com",
              "id": 1,
              "is_timestamp": true,
              "name": "Ava Chen",
              "type": "string",
              "url": "https://example.com",
              "val_id": 1,
              "value": "string"
            },
            "badge_icon_type": 1,
            "brand": "string",
            "brand_id": 1,
            "bundle_deal_info": "string",
            "can_use_wholesale": true,
            "cat_id": 1,
            "categories": {
              "catid": 1,
              "display_name": "Ava Chen",
              "is_default_subcat": true,
              "no_sub": true
            },
            "cb_option": 1,
            "complaint_policy": "string",
            "condition": 1,
            "ctime": 1,
            "currency": "string",
            "current_promotion_has_reserve_stock": true,
            "current_promotion_reserved_stock": 1,
            "deep_discount": "string",
            "description": "string",
            "discount_stock": 1,
            "estimated_days": 1,
            "fe_categories": {
              "catid": 1,
              "display_name": "Ava Chen",
              "is_default_subcat": true,
              "no_sub": true
            },
            "flag": 1,
            "has_low_fulfillment_rate": true,
            "has_model_with_available_shopee_stock": true,
            "hidden_price_display": "string",
            "image": "string",
            "invoice_option": "string",
            "is_adult": true,
            "is_alcohol_product": true,
            "is_category_failed": "string",
            "is_free_gift": true,
            "is_free_shipping": true,
            "is_hide_stock": true,
            "is_infant_milk_formula_product": true,
            "is_item_inherited": true,
            "is_live_streaming_price": "string",
            "is_low_price_eligible": "string",
            "is_lowest_price_at_shopee": "string",
            "is_partial_fulfilled": true,
            "is_pre_order": true,
            "is_presale": true,
            "is_presale_deposit_item": "string",
            "is_presale_deposit_made": "string",
            "is_prescription_item": true,
            "is_preview": true,
            "is_service_by_shopee": true,
            "is_unavailable": true,
            "item_has_video": true,
            "item_id": 1,
            "item_rating": {
              "rating_star": 1
            },
            "item_status": "string",
            "item_type": 1,
            "label_ids": [
              1
            ],
            "max_quantity": 1,
            "min_purchase_limit": 1,
            "models": {
              "current_promotion_has_reserve_stock": true,
              "current_promotion_reserved_stock": "string",
              "extinfo": {
                "estimated_days": 1,
                "is_pre_order": true,
                "tier_index": [
                  1
                ]
              },
              "has_gimmick_tag": true,
              "is_lowest_price_at_shopee": true,
              "item_id": 1,
              "key_measurement": "string",
              "model_id": 1,
              "name": "Ava Chen",
              "normal_stock": "string",
              "price": 1,
              "price_before_discount": 1,
              "price_stocks": {
                "allocated_stock": 1,
                "promotion_type": 1,
                "stock_breakdown_by_location": {
                  "address_id": 1,
                  "allocated_stock": "string",
                  "available_stock": "string",
                  "fulfilment_type": 1,
                  "location_id": "string"
                }
              },
              "promotion_id": 1,
              "sold": "string",
              "status": 1,
              "stock": "string"
            },
            "normal_stock": "string",
            "other_stock": "string",
            "overall_purchase_limit": "string",
            "presale_dday_start_time": "string",
            "preview_info": "string",
            "price": 1,
            "price_before_discount": 1,
            "price_max": 1,
            "price_max_before_discount": 1,
            "price_min": 1,
            "price_min_before_discount": 1,
            "raw_discount": 1,
            "reference_item_id": "string",
            "rich_text_description": {
              "paragraph_list": {
                "empty_paragraph_count": 1,
                "img_id": "string",
                "ratio": "string",
                "text": "string",
                "type": 1
              }
            },
            "shipping_icon_type": 1,
            "shop_id": 1,
            "shop_location": "string",
            "should_show_amp_tag": true,
            "show_discount": 1,
            "show_prescription_feed": true,
            "show_recycling_info": true,
            "size_chart": "string",
            "size_chart_info": "string",
            "spl_info": {
              "channel_id": "string",
              "installment_info": "string",
              "show_spl": true,
              "show_spl_lite": "string",
              "spl_xtra": "string",
              "user_credit_info": "string"
            },
            "status": 1,
            "stock": "string",
            "tier_variations": {
              "display_indicators": [
                1
              ],
              "images": "string",
              "name": "Ava Chen",
              "options": [
                "string"
              ],
              "properties": "string",
              "summed_stocks": "string",
              "type": 1
            },
            "title": "string",
            "welcome_package_type": 1,
            "wholesale_tier_list": [
              "string"
            ]
          },
          "membership_exclusive": "string",
          "membership_exclusive_teaser": "string",
          "nea": "string",
          "ongoing_banner": "string",
          "price_breakdown": "string",
          "product_attributes": {
            "attrs": {
              "brand_id": 1,
              "brand_option": "string",
              "full_url": "https://example.com",
              "id": 1,
              "is_timestamp": "string",
              "name": "Ava Chen",
              "type": 1,
              "url": "https://example.com",
              "val_id": "string",
              "value": "string"
            },
            "categories": {
              "catid": 1,
              "display_name": "Ava Chen",
              "is_default_subcat": true,
              "no_sub": true
            },
            "related_items": [
              "string"
            ]
          },
          "product_images": {
            "abnormal_status": "string",
            "first_tier_variations": [
              "string"
            ],
            "has_long_image": "string",
            "images": [
              "string"
            ],
            "long_images": "string",
            "makeup_preview": "string",
            "overlay": "string",
            "pdp_top_info_list": "string",
            "promotion_images": [
              "string"
            ],
            "shopee_video_info_list": [
              "string"
            ],
            "shopee_video_rcmd_info": "string",
            "shopee_video_req_id": "string",
            "skincam": "string",
            "sorted_variation_image_index_list": [
              "string"
            ],
            "video": "string"
          },
          "product_meta": {
            "hide_sharing_button": true,
            "hide_sold_count": true,
            "show_best_price_guarantee": true,
            "show_lowest_installment_guarantee": true,
            "show_lowest_price_guarantee": true,
            "show_official_shop_label_in_title": true,
            "show_original_guarantee": true,
            "show_shopee_verified_label": true
          },
          "product_price": {
            "discount": "string",
            "discount_text": "string",
            "hide_discount": true,
            "hide_price": true,
            "installment_info": "string",
            "labels": "string",
            "lowest_past_price": "string",
            "pack_size": "string",
            "presale_price": "string",
            "price": {
              "price_mask": "string",
              "range_max": 1,
              "range_min": 1,
              "single_value": 1
            },
            "price_before_discount": "string",
            "show_final_price_indicator": true,
            "spl_installment_info": "string"
          },
          "product_review": {
            "cmt_count": 1,
            "display_global_sold": true,
            "global_sold": "string",
            "hide_buyer_gallery": true,
            "hide_other_product_reviews_in_shop": true,
            "hide_rating": true,
            "hide_reviews": true,
            "historical_sold": "string",
            "liked": true,
            "liked_count": 1,
            "rating_count": [
              1
            ],
            "rating_star": 1,
            "review_rcmd_exp_group": "string",
            "should_move_ratings_above": "string",
            "total_rating_count": 1
          },
          "product_shipping": {
            "also_available_channel_icon_type": "string",
            "also_available_channel_name": "Ava Chen",
            "free_shipping": {
              "has_fss": true,
              "min_spend": {
                "price_mask": "string",
                "range_max": 1,
                "range_min": 1,
                "single_value": 1
              }
            },
            "grouped_channel_infos_by_service_type": [
              "string"
            ],
            "is_item_with_price_range": true,
            "pre_order_text": "string",
            "pre_selected_shipping_channel": "string",
            "selected_late_delivery_compensation_for_drawer": "string",
            "shipping_fee_info": {
              "price": {
                "price_mask": "string",
                "range_max": 1,
                "range_min": 1,
                "single_value": 1
              },
              "ship_from_location": "string",
              "shipping_icon_type": 1,
              "warning": "string"
            },
            "shipping_info_text": {
              "edt_from": "string",
              "edt_to": "string",
              "shipping_fee": "string",
              "show_shipping_fee_suffix": true,
              "text_template": "string"
            },
            "show_grouped_channel_first": "string",
            "show_shipping_to": true,
            "ungrouped_channel_infos": {
              "channel_delivery_info": {
                "delay_message": "string",
                "display_mode": "string",
                "edt_text": "string",
                "estimated_delivery_date_from": 1,
                "estimated_delivery_date_to": 1,
                "estimated_delivery_time_max": 1,
                "estimated_delivery_time_min": 1,
                "has_edt": true,
                "is_fastest_edt_channel": "string",
                "show_edt": true,
                "sla_message": "string"
              },
              "channel_id": 1,
              "channel_promotion_infos": {
                "cap": 1,
                "discount_off": 1,
                "display_mode": 1,
                "min_spend": {
                  "price_mask": "string",
                  "range_max": 1,
                  "range_min": 1,
                  "single_value": 1
                },
                "rule_id": 1,
                "type": 1
              },
              "display_text": {
                "direct_delivery": "string",
                "fulfilled_by_shopee": "string",
                "late_delivery_compensation": "string"
              },
              "is_integrated_channel": true,
              "is_sst_included": true,
              "late_delivery_compensation": "string",
              "lowest_bpsf_promotion_rule": "string",
              "name": "Ava Chen",
              "price": {
                "price_mask": "string",
                "range_max": 1,
                "range_min": 1,
                "single_value": 1
              },
              "price_before_discount": {
                "price_mask": "string",
                "range_max": 1,
                "range_min": 1,
                "single_value": 1
              },
              "rule_type": 1,
              "service_type_info": "string",
              "shipping_icon_type": "string",
              "warning": "string"
            }
          },
          "promotion_info": {
            "installment": "string",
            "insurance": "string",
            "item_installment_eligibility": {
              "is_cc_installment_payment_eligible": true,
              "is_non_cc_installment_payment_eligible": true
            },
            "spl": "string",
            "spl_lite": "string",
            "wholesale": "string"
          },
          "removed_fields": "string",
          "return_on_spot": "string",
          "shipping_info": "string",
          "shipping_meta": "string",
          "shop_detailed": {
            "account": {
              "portrait": "string",
              "status": 1,
              "username": "Ava Chen"
            },
            "authorized_brand": "string",
            "banner": {
              "shopee_choice": "string"
            },
            "ctime": 1,
            "favorite_shop_info": "string",
            "follower_count": 1,
            "is_3pf": true,
            "is_high_end": true,
            "is_individual_seller": "string",
            "is_mart": true,
            "is_official_shop": true,
            "is_preferred_plus_seller": true,
            "is_shopee_choice": true,
            "is_shopee_verified": true,
            "item_count": 1,
            "last_active_time": 1,
            "name": "Ava Chen",
            "place": "string",
            "rating_bad": 1,
            "rating_good": 1,
            "rating_normal": 1,
            "rating_star": 1,
            "response_rate": 1,
            "response_time": 1,
            "session_info": "string",
            "session_infos": "string",
            "shop_location": "string",
            "shopid": 1,
            "show_official_shop_label": true,
            "sold_total": "string",
            "status": 1,
            "userid": 1,
            "vacation": true
          },
          "shop_vouchers": [
            "string"
          ],
          "shopee_free_return": "string",
          "size_guide": "string",
          "tax_disclaimer": "string",
          "teaser_banner": "string",
          "vehicle_compatibility_info": "string"
        },
        "error": "string",
        "error_msg": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | object |  |
| `data.bff_meta` | string |  |
| `data.data` | object |  |
| `data.data.abnormal_popup` | string |  |
| `data.data.account` | object |  |
| `data.data.account.adult_consent` | string |  |
| `data.data.account.birth_timestamp` | string |  |
| `data.data.account.default_address` | object |  |
| `data.data.account.default_address.address` | string |  |
| `data.data.account.default_address.city` | string |  |
| `data.data.account.default_address.district` | string |  |
| `data.data.account.default_address.latitude` | string |  |
| `data.data.account.default_address.longitude` | string |  |
| `data.data.account.default_address.region` | string |  |
| `data.data.account.default_address.state` | string |  |
| `data.data.account.default_address.town` | string |  |
| `data.data.account.default_address.zip_code` | string |  |
| `data.data.account.is_new_user` | string |  |
| `data.data.account.user_id` | string |  |
| `data.data.age_gate` | object |  |
| `data.data.age_gate_control` | string |  |
| `data.data.age_gate.kyc` | string |  |
| `data.data.alcohol_disclaimer` | string |  |
| `data.data.button_group` | object |  |
| `data.data.button_group.buy_with_voucher` | string |  |
| `data.data.coin_info` | object |  |
| `data.data.coin_info.coin_earn_items` | array<string> |  |
| `data.data.coin_info.coin_earn_label` | string |  |
| `data.data.coin_info.spend_cash_unit` | number |  |
| `data.data.deep_discount` | string |  |
| `data.data.design_control` | object |  |
| `data.data.design_control.disable_price_with_variation` | boolean |  |
| `data.data.design_control.display_choice_customised_section` | boolean |  |
| `data.data.design_control.display_direct_delivery` | boolean |  |
| `data.data.design_control.display_on_time_delivery_guarantee` | boolean |  |
| `data.data.design_control.enable_ksp_config` | string |  |
| `data.data.design_control.first_screen_revamp_abtest_group` | string |  |
| `data.data.design_control.is_support_fbs_enabled` | boolean |  |
| `data.data.design_control.top_section_featured_video_ab_test_group` | string |  |
| `data.data.design_control.use_new_featured_video_revamp` | string |  |
| `data.data.design_control.use_new_revamp_first_screen` | string |  |
| `data.data.designer_info` | string |  |
| `data.data.detail_level` | number |  |
| `data.data.display_sections` | object |  |
| `data.data.display_sections.add_on_deal` | string |  |
| `data.data.display_sections.bundle_deal` | string |  |
| `data.data.display_sections.coin` | string |  |
| `data.data.display_sections.exclusive_price_label` | string |  |
| `data.data.display_sections.free_return` | string |  |
| `data.data.display_sections.wholesale` | string |  |
| `data.data.exclusive_price` | string |  |
| `data.data.exclusive_price_cta` | string |  |
| `data.data.flash_sale` | string |  |
| `data.data.flash_sale_preview` | string |  |
| `data.data.free_return` | string |  |
| `data.data.ineligible_ep` | string |  |
| `data.data.installment_drawer` | string |  |
| `data.data.item` | object |  |
| `data.data.item.add_on_deal_info` | string |  |
| `data.data.item.all_models_has_pre_order` | boolean |  |
| `data.data.item.attributes` | array<object> |  |
| `data.data.item.attributes.brand_id` | string |  |
| `data.data.item.attributes.brand_option` | string |  |
| `data.data.item.attributes.full_url` | string |  |
| `data.data.item.attributes.id` | number |  |
| `data.data.item.attributes.is_timestamp` | boolean |  |
| `data.data.item.attributes.name` | string |  |
| `data.data.item.attributes.type` | string |  |
| `data.data.item.attributes.url` | string |  |
| `data.data.item.attributes.val_id` | number |  |
| `data.data.item.attributes.value` | string |  |
| `data.data.item.badge_icon_type` | number |  |
| `data.data.item.brand` | string |  |
| `data.data.item.brand_id` | number |  |
| `data.data.item.bundle_deal_info` | string |  |
| `data.data.item.can_use_wholesale` | boolean |  |
| `data.data.item.cat_id` | number |  |
| `data.data.item.categories` | array<object> |  |
| `data.data.item.categories.catid` | number |  |
| `data.data.item.categories.display_name` | string |  |
| `data.data.item.categories.is_default_subcat` | boolean |  |
| `data.data.item.categories.no_sub` | boolean |  |
| `data.data.item.cb_option` | number |  |
| `data.data.item.complaint_policy` | string |  |
| `data.data.item.condition` | number |  |
| `data.data.item.ctime` | number |  |
| `data.data.item.currency` | string |  |
| `data.data.item.current_promotion_has_reserve_stock` | boolean |  |
| `data.data.item.current_promotion_reserved_stock` | number |  |
| `data.data.item.deep_discount` | string |  |
| `data.data.item.description` | string |  |
| `data.data.item.discount_stock` | number |  |
| `data.data.item.estimated_days` | number |  |
| `data.data.item.fe_categories` | array<object> |  |
| `data.data.item.fe_categories.catid` | number |  |
| `data.data.item.fe_categories.display_name` | string |  |
| `data.data.item.fe_categories.is_default_subcat` | boolean |  |
| `data.data.item.fe_categories.no_sub` | boolean |  |
| `data.data.item.flag` | number |  |
| `data.data.item.has_low_fulfillment_rate` | boolean |  |
| `data.data.item.has_model_with_available_shopee_stock` | boolean |  |
| `data.data.item.hidden_price_display` | string |  |
| `data.data.item.image` | string |  |
| `data.data.item.invoice_option` | string |  |
| `data.data.item.is_adult` | boolean |  |
| `data.data.item.is_alcohol_product` | boolean |  |
| `data.data.item.is_category_failed` | string |  |
| `data.data.item.is_free_gift` | boolean |  |
| `data.data.item.is_free_shipping` | boolean |  |
| `data.data.item.is_hide_stock` | boolean |  |
| `data.data.item.is_infant_milk_formula_product` | boolean |  |
| `data.data.item.is_item_inherited` | boolean |  |
| `data.data.item.is_live_streaming_price` | string |  |
| `data.data.item.is_low_price_eligible` | string |  |
| `data.data.item.is_lowest_price_at_shopee` | string |  |
| `data.data.item.is_partial_fulfilled` | boolean |  |
| `data.data.item.is_pre_order` | boolean |  |
| `data.data.item.is_presale` | boolean |  |
| `data.data.item.is_presale_deposit_item` | string |  |
| `data.data.item.is_presale_deposit_made` | string |  |
| `data.data.item.is_prescription_item` | boolean |  |
| `data.data.item.is_preview` | boolean |  |
| `data.data.item.is_service_by_shopee` | boolean |  |
| `data.data.item.is_unavailable` | boolean |  |
| `data.data.item.item_has_video` | boolean |  |
| `data.data.item.item_id` | number |  |
| `data.data.item.item_rating` | object |  |
| `data.data.item.item_rating.rating_star` | number |  |
| `data.data.item.item_status` | string |  |
| `data.data.item.item_type` | number |  |
| `data.data.item.label_ids` | array<number> |  |
| `data.data.item.max_quantity` | number |  |
| `data.data.item.min_purchase_limit` | number |  |
| `data.data.item.models` | array<object> |  |
| `data.data.item.models.current_promotion_has_reserve_stock` | boolean |  |
| `data.data.item.models.current_promotion_reserved_stock` | string |  |
| `data.data.item.models.extinfo` | object |  |
| `data.data.item.models.extinfo.estimated_days` | number |  |
| `data.data.item.models.extinfo.is_pre_order` | boolean |  |
| `data.data.item.models.extinfo.tier_index` | array<number> |  |
| `data.data.item.models.has_gimmick_tag` | boolean |  |
| `data.data.item.models.is_lowest_price_at_shopee` | boolean |  |
| `data.data.item.models.item_id` | number |  |
| `data.data.item.models.key_measurement` | string |  |
| `data.data.item.models.model_id` | number |  |
| `data.data.item.models.name` | string |  |
| `data.data.item.models.normal_stock` | string |  |
| `data.data.item.models.price` | number |  |
| `data.data.item.models.price_before_discount` | number |  |
| `data.data.item.models.price_stocks` | array<object> |  |
| `data.data.item.models.price_stocks.allocated_stock` | number |  |
| `data.data.item.models.price_stocks.promotion_type` | number |  |
| `data.data.item.models.price_stocks.stock_breakdown_by_location` | array<object> |  |
| `data.data.item.models.price_stocks.stock_breakdown_by_location.address_id` | number |  |
| `data.data.item.models.price_stocks.stock_breakdown_by_location.allocated_stock` | string |  |
| `data.data.item.models.price_stocks.stock_breakdown_by_location.available_stock` | string |  |
| `data.data.item.models.price_stocks.stock_breakdown_by_location.fulfilment_type` | number |  |
| `data.data.item.models.price_stocks.stock_breakdown_by_location.location_id` | string |  |
| `data.data.item.models.promotion_id` | number |  |
| `data.data.item.models.sold` | string |  |
| `data.data.item.models.status` | number |  |
| `data.data.item.models.stock` | string |  |
| `data.data.item.normal_stock` | string |  |
| `data.data.item.other_stock` | string |  |
| `data.data.item.overall_purchase_limit` | string |  |
| `data.data.item.presale_dday_start_time` | string |  |
| `data.data.item.preview_info` | string |  |
| `data.data.item.price` | number |  |
| `data.data.item.price_before_discount` | number |  |
| `data.data.item.price_max` | number |  |
| `data.data.item.price_max_before_discount` | number |  |
| `data.data.item.price_min` | number |  |
| `data.data.item.price_min_before_discount` | number |  |
| `data.data.item.raw_discount` | number |  |
| `data.data.item.reference_item_id` | string |  |
| `data.data.item.rich_text_description` | object |  |
| `data.data.item.rich_text_description.paragraph_list` | array<object> |  |
| `data.data.item.rich_text_description.paragraph_list.empty_paragraph_count` | number |  |
| `data.data.item.rich_text_description.paragraph_list.img_id` | string |  |
| `data.data.item.rich_text_description.paragraph_list.ratio` | string |  |
| `data.data.item.rich_text_description.paragraph_list.text` | string |  |
| `data.data.item.rich_text_description.paragraph_list.type` | number |  |
| `data.data.item.shipping_icon_type` | number |  |
| `data.data.item.shop_id` | number |  |
| `data.data.item.shop_location` | string |  |
| `data.data.item.should_show_amp_tag` | boolean |  |
| `data.data.item.show_discount` | number |  |
| `data.data.item.show_prescription_feed` | boolean |  |
| `data.data.item.show_recycling_info` | boolean |  |
| `data.data.item.size_chart` | string |  |
| `data.data.item.size_chart_info` | string |  |
| `data.data.item.spl_info` | object |  |
| `data.data.item.spl_info.channel_id` | string |  |
| `data.data.item.spl_info.installment_info` | string |  |
| `data.data.item.spl_info.show_spl` | boolean |  |
| `data.data.item.spl_info.show_spl_lite` | string |  |
| `data.data.item.spl_info.spl_xtra` | string |  |
| `data.data.item.spl_info.user_credit_info` | string |  |
| `data.data.item.status` | number |  |
| `data.data.item.stock` | string |  |
| `data.data.item.tier_variations` | array<object> |  |
| `data.data.item.tier_variations.display_indicators` | array<number> |  |
| `data.data.item.tier_variations.images` | string |  |
| `data.data.item.tier_variations.name` | string |  |
| `data.data.item.tier_variations.options` | array<string> |  |
| `data.data.item.tier_variations.properties` | string |  |
| `data.data.item.tier_variations.summed_stocks` | string |  |
| `data.data.item.tier_variations.type` | number |  |
| `data.data.item.title` | string |  |
| `data.data.item.welcome_package_type` | number |  |
| `data.data.item.wholesale_tier_list` | array<string> |  |
| `data.data.membership_exclusive` | string |  |
| `data.data.membership_exclusive_teaser` | string |  |
| `data.data.nea` | string |  |
| `data.data.ongoing_banner` | string |  |
| `data.data.price_breakdown` | string |  |
| `data.data.product_attributes` | object |  |
| `data.data.product_attributes.attrs` | array<object> |  |
| `data.data.product_attributes.attrs.brand_id` | number |  |
| `data.data.product_attributes.attrs.brand_option` | string |  |
| `data.data.product_attributes.attrs.full_url` | string |  |
| `data.data.product_attributes.attrs.id` | number |  |
| `data.data.product_attributes.attrs.is_timestamp` | string |  |
| `data.data.product_attributes.attrs.name` | string |  |
| `data.data.product_attributes.attrs.type` | number |  |
| `data.data.product_attributes.attrs.url` | string |  |
| `data.data.product_attributes.attrs.val_id` | string |  |
| `data.data.product_attributes.attrs.value` | string |  |
| `data.data.product_attributes.categories` | array<object> |  |
| `data.data.product_attributes.categories.catid` | number |  |
| `data.data.product_attributes.categories.display_name` | string |  |
| `data.data.product_attributes.categories.is_default_subcat` | boolean |  |
| `data.data.product_attributes.categories.no_sub` | boolean |  |
| `data.data.product_attributes.related_items` | array<string> |  |
| `data.data.product_images` | object |  |
| `data.data.product_images.abnormal_status` | string |  |
| `data.data.product_images.first_tier_variations` | array<string> |  |
| `data.data.product_images.has_long_image` | string |  |
| `data.data.product_images.images` | array<string> |  |
| `data.data.product_images.long_images` | string |  |
| `data.data.product_images.makeup_preview` | string |  |
| `data.data.product_images.overlay` | string |  |
| `data.data.product_images.pdp_top_info_list` | string |  |
| `data.data.product_images.promotion_images` | array<string> |  |
| `data.data.product_images.shopee_video_info_list` | array<string> |  |
| `data.data.product_images.shopee_video_rcmd_info` | string |  |
| `data.data.product_images.shopee_video_req_id` | string |  |
| `data.data.product_images.skincam` | string |  |
| `data.data.product_images.sorted_variation_image_index_list` | array<string> |  |
| `data.data.product_images.video` | string |  |
| `data.data.product_meta` | object |  |
| `data.data.product_meta.hide_sharing_button` | boolean |  |
| `data.data.product_meta.hide_sold_count` | boolean |  |
| `data.data.product_meta.show_best_price_guarantee` | boolean |  |
| `data.data.product_meta.show_lowest_installment_guarantee` | boolean |  |
| `data.data.product_meta.show_lowest_price_guarantee` | boolean |  |
| `data.data.product_meta.show_official_shop_label_in_title` | boolean |  |
| `data.data.product_meta.show_original_guarantee` | boolean |  |
| `data.data.product_meta.show_shopee_verified_label` | boolean |  |
| `data.data.product_price` | object |  |
| `data.data.product_price.discount` | string |  |
| `data.data.product_price.discount_text` | string |  |
| `data.data.product_price.hide_discount` | boolean |  |
| `data.data.product_price.hide_price` | boolean |  |
| `data.data.product_price.installment_info` | string |  |
| `data.data.product_price.labels` | string |  |
| `data.data.product_price.lowest_past_price` | string |  |
| `data.data.product_price.pack_size` | string |  |
| `data.data.product_price.presale_price` | string |  |
| `data.data.product_price.price` | object |  |
| `data.data.product_price.price_before_discount` | string |  |
| `data.data.product_price.price.price_mask` | string |  |
| `data.data.product_price.price.range_max` | number |  |
| `data.data.product_price.price.range_min` | number |  |
| `data.data.product_price.price.single_value` | number |  |
| `data.data.product_price.show_final_price_indicator` | boolean |  |
| `data.data.product_price.spl_installment_info` | string |  |
| `data.data.product_review` | object |  |
| `data.data.product_review.cmt_count` | number |  |
| `data.data.product_review.display_global_sold` | boolean |  |
| `data.data.product_review.global_sold` | string |  |
| `data.data.product_review.hide_buyer_gallery` | boolean |  |
| `data.data.product_review.hide_other_product_reviews_in_shop` | boolean |  |
| `data.data.product_review.hide_rating` | boolean |  |
| `data.data.product_review.hide_reviews` | boolean |  |
| `data.data.product_review.historical_sold` | string |  |
| `data.data.product_review.liked` | boolean |  |
| `data.data.product_review.liked_count` | number |  |
| `data.data.product_review.rating_count` | array<number> |  |
| `data.data.product_review.rating_star` | number |  |
| `data.data.product_review.review_rcmd_exp_group` | string |  |
| `data.data.product_review.should_move_ratings_above` | string |  |
| `data.data.product_review.total_rating_count` | number |  |
| `data.data.product_shipping` | object |  |
| `data.data.product_shipping.also_available_channel_icon_type` | string |  |
| `data.data.product_shipping.also_available_channel_name` | string |  |
| `data.data.product_shipping.free_shipping` | object |  |
| `data.data.product_shipping.free_shipping.has_fss` | boolean |  |
| `data.data.product_shipping.free_shipping.min_spend` | object |  |
| `data.data.product_shipping.free_shipping.min_spend.price_mask` | string |  |
| `data.data.product_shipping.free_shipping.min_spend.range_max` | number |  |
| `data.data.product_shipping.free_shipping.min_spend.range_min` | number |  |
| `data.data.product_shipping.free_shipping.min_spend.single_value` | number |  |
| `data.data.product_shipping.grouped_channel_infos_by_service_type` | array<string> |  |
| `data.data.product_shipping.is_item_with_price_range` | boolean |  |
| `data.data.product_shipping.pre_order_text` | string |  |
| `data.data.product_shipping.pre_selected_shipping_channel` | string |  |
| `data.data.product_shipping.selected_late_delivery_compensation_for_drawer` | string |  |
| `data.data.product_shipping.shipping_fee_info` | object |  |
| `data.data.product_shipping.shipping_fee_info.price` | object |  |
| `data.data.product_shipping.shipping_fee_info.price.price_mask` | string |  |
| `data.data.product_shipping.shipping_fee_info.price.range_max` | number |  |
| `data.data.product_shipping.shipping_fee_info.price.range_min` | number |  |
| `data.data.product_shipping.shipping_fee_info.price.single_value` | number |  |
| `data.data.product_shipping.shipping_fee_info.ship_from_location` | string |  |
| `data.data.product_shipping.shipping_fee_info.shipping_icon_type` | number |  |
| `data.data.product_shipping.shipping_fee_info.warning` | string |  |
| `data.data.product_shipping.shipping_info_text` | object |  |
| `data.data.product_shipping.shipping_info_text.edt_from` | string |  |
| `data.data.product_shipping.shipping_info_text.edt_to` | string |  |
| `data.data.product_shipping.shipping_info_text.shipping_fee` | string |  |
| `data.data.product_shipping.shipping_info_text.show_shipping_fee_suffix` | boolean |  |
| `data.data.product_shipping.shipping_info_text.text_template` | string |  |
| `data.data.product_shipping.show_grouped_channel_first` | string |  |
| `data.data.product_shipping.show_shipping_to` | boolean |  |
| `data.data.product_shipping.ungrouped_channel_infos` | array<object> |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info` | object |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.delay_message` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.display_mode` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.edt_text` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.estimated_delivery_date_from` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.estimated_delivery_date_to` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.estimated_delivery_time_max` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.estimated_delivery_time_min` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.has_edt` | boolean |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.is_fastest_edt_channel` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.show_edt` | boolean |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_delivery_info.sla_message` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_id` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos` | array<object> |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.cap` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.discount_off` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.display_mode` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.min_spend` | object |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.min_spend.price_mask` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.min_spend.range_max` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.min_spend.range_min` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.min_spend.single_value` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.rule_id` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.channel_promotion_infos.type` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.display_text` | object |  |
| `data.data.product_shipping.ungrouped_channel_infos.display_text.direct_delivery` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.display_text.fulfilled_by_shopee` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.display_text.late_delivery_compensation` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.is_integrated_channel` | boolean |  |
| `data.data.product_shipping.ungrouped_channel_infos.is_sst_included` | boolean |  |
| `data.data.product_shipping.ungrouped_channel_infos.late_delivery_compensation` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.lowest_bpsf_promotion_rule` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.name` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.price` | object |  |
| `data.data.product_shipping.ungrouped_channel_infos.price_before_discount` | object |  |
| `data.data.product_shipping.ungrouped_channel_infos.price_before_discount.price_mask` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.price_before_discount.range_max` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.price_before_discount.range_min` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.price_before_discount.single_value` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.price.price_mask` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.price.range_max` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.price.range_min` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.price.single_value` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.rule_type` | number |  |
| `data.data.product_shipping.ungrouped_channel_infos.service_type_info` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.shipping_icon_type` | string |  |
| `data.data.product_shipping.ungrouped_channel_infos.warning` | string |  |
| `data.data.promotion_info` | object |  |
| `data.data.promotion_info.installment` | string |  |
| `data.data.promotion_info.insurance` | string |  |
| `data.data.promotion_info.item_installment_eligibility` | object |  |
| `data.data.promotion_info.item_installment_eligibility.is_cc_installment_payment_eligible` | boolean |  |
| `data.data.promotion_info.item_installment_eligibility.is_non_cc_installment_payment_eligible` | boolean |  |
| `data.data.promotion_info.spl` | string |  |
| `data.data.promotion_info.spl_lite` | string |  |
| `data.data.promotion_info.wholesale` | string |  |
| `data.data.removed_fields` | string |  |
| `data.data.return_on_spot` | string |  |
| `data.data.shipping_info` | string |  |
| `data.data.shipping_meta` | string |  |
| `data.data.shop_detailed` | object |  |
| `data.data.shop_detailed.account` | object |  |
| `data.data.shop_detailed.account.portrait` | string |  |
| `data.data.shop_detailed.account.status` | number |  |
| `data.data.shop_detailed.account.username` | string |  |
| `data.data.shop_detailed.authorized_brand` | string |  |
| `data.data.shop_detailed.banner` | object |  |
| `data.data.shop_detailed.banner.shopee_choice` | string |  |
| `data.data.shop_detailed.ctime` | number |  |
| `data.data.shop_detailed.favorite_shop_info` | string |  |
| `data.data.shop_detailed.follower_count` | number |  |
| `data.data.shop_detailed.is_3pf` | boolean |  |
| `data.data.shop_detailed.is_high_end` | boolean |  |
| `data.data.shop_detailed.is_individual_seller` | string |  |
| `data.data.shop_detailed.is_mart` | boolean |  |
| `data.data.shop_detailed.is_official_shop` | boolean |  |
| `data.data.shop_detailed.is_preferred_plus_seller` | boolean |  |
| `data.data.shop_detailed.is_shopee_choice` | boolean |  |
| `data.data.shop_detailed.is_shopee_verified` | boolean |  |
| `data.data.shop_detailed.item_count` | number |  |
| `data.data.shop_detailed.last_active_time` | number |  |
| `data.data.shop_detailed.name` | string |  |
| `data.data.shop_detailed.place` | string |  |
| `data.data.shop_detailed.rating_bad` | number |  |
| `data.data.shop_detailed.rating_good` | number |  |
| `data.data.shop_detailed.rating_normal` | number |  |
| `data.data.shop_detailed.rating_star` | number |  |
| `data.data.shop_detailed.response_rate` | number |  |
| `data.data.shop_detailed.response_time` | number |  |
| `data.data.shop_detailed.session_info` | string |  |
| `data.data.shop_detailed.session_infos` | string |  |
| `data.data.shop_detailed.shop_location` | string |  |
| `data.data.shop_detailed.shopid` | number |  |
| `data.data.shop_detailed.show_official_shop_label` | boolean |  |
| `data.data.shop_detailed.sold_total` | string |  |
| `data.data.shop_detailed.status` | number |  |
| `data.data.shop_detailed.userid` | number |  |
| `data.data.shop_detailed.vacation` | boolean |  |
| `data.data.shop_vouchers` | array<string> |  |
| `data.data.shopee_free_return` | string |  |
| `data.data.size_guide` | string |  |
| `data.data.tax_disclaimer` | string |  |
| `data.data.teaser_banner` | string |  |
| `data.data.vehicle_compatibility_info` | string |  |
| `data.error` | string |  |
| `data.error_msg` | string |  |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /api/v1/scraper/result/:taskId` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scraper-result.md) for the provider-specific parameters and requirements.

