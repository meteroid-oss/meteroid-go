# Changelog

## [0.31.1](https://github.com/meteroid-oss/meteroid-go/compare/v0.31.0...v0.31.1) (2026-10-30)


### Features

* **api:** add `GET /api/v1/licenses`, `GET /api/v1/licenses/{license_id}`, `GET /api/v1/licenses/{license_id}/activation-code`, `GET /api/v1/licensing/signing-keys`, `POST /api/v1/licenses` and 2 more ([ccfcc8a](https://github.com/meteroid-oss/meteroid-go/commit/ccfcc8aeb4672273c0489a890533d1dee9f39951))
* **api:** update `GET /api/v1/plans`, `GET /api/v1/plans/{plan_id}`, `PATCH /api/v1/plans/{plan_id}`, `POST /api/v1/custom-property-definitions`, `POST /api/v1/plans` and 3 more ([ccfcc8a](https://github.com/meteroid-oss/meteroid-go/commit/ccfcc8aeb4672273c0489a890533d1dee9f39951))
* **api:** update SDKs to meteroid 0.1.0 ([#17](https://github.com/meteroid-oss/meteroid-go/issues/17)) ([ccfcc8a](https://github.com/meteroid-oss/meteroid-go/commit/ccfcc8aeb4672273c0489a890533d1dee9f39951))

## [0.31.0](https://github.com/meteroid-oss/meteroid-go/compare/v0.30.1...v0.31.0) (2026-10-28)


### ⚠ BREAKING CHANGES

* **api:** update SDKs to meteroid 0.1.0 ([#15](https://github.com/meteroid-oss/meteroid-go/issues/15))
* **api:** `GET /api/v1/coupons`: added `#/components/schemas/CreditDiscount` to the `data/items/discount` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/coupons/{coupon_id}`: added `#/components/schemas/CreditDiscount` to the `discount` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/plans`: added `#/components/schemas/CreditPlanFee` to the `data/items/price_components/items/fee/oneOf[#/components/schemas/Fee]/` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/plans/{plan_id}`: added `#/components/schemas/CreditPlanFee` to the `price_components/items/fee/oneOf[#/components/schemas/Fee]/` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/products`: added `#/components/schemas/CreditFeeStructure` to the `data/items/fee_structure` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/products/{product_id}`: added `#/components/schemas/CreditFeeStructure` to the `fee_structure` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/subscriptions/{subscription_id}`: added `#/components/schemas/CreditDiscount` to the `applied_coupons/items/coupon/discount` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/subscriptions/{subscription_id}`: added `#/components/schemas/CreditFee` to the `add_ons/items/fee` response property `oneOf` list for the response status `200`
* **api:** `GET /api/v1/subscriptions/{subscription_id}`: added `#/components/schemas/CreditFee` to the `components/items/fee` response property `oneOf` list for the response status `200`
* **api:** `PATCH /api/v1/coupons/{coupon_id}`: added the new required request property `discount/oneOf[#/components/schemas/CouponDiscount]/oneOf[#/components/schemas/FixedDiscount]/type`
* **api:** 90 more breaking changes

### Features

* **api:** `GET /api/v1/coupons/{coupon_id}`: added `#/components/schemas/CreditDiscount` to the `discount` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/coupons`: added `#/components/schemas/CreditDiscount` to the `data/items/discount` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/plans/{plan_id}`: added `#/components/schemas/CreditPlanFee` to the `price_components/items/fee/oneOf[#/components/schemas/Fee]/` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/plans`: added `#/components/schemas/CreditPlanFee` to the `data/items/price_components/items/fee/oneOf[#/components/schemas/Fee]/` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/products/{product_id}`: added `#/components/schemas/CreditFeeStructure` to the `fee_structure` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/products`: added `#/components/schemas/CreditFeeStructure` to the `data/items/fee_structure` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/subscriptions/{subscription_id}`: added `#/components/schemas/CreditDiscount` to the `applied_coupons/items/coupon/discount` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/subscriptions/{subscription_id}`: added `#/components/schemas/CreditFee` to the `add_ons/items/fee` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `GET /api/v1/subscriptions/{subscription_id}`: added `#/components/schemas/CreditFee` to the `components/items/fee` response property `oneOf` list for the response status `200` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** `PATCH /api/v1/coupons/{coupon_id}`: added the new required request property `discount/oneOf[#/components/schemas/CouponDiscount]/oneOf[#/components/schemas/FixedDiscount]/type` ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** 90 more breaking changes ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** update SDKs to meteroid 0.1.0 ([#15](https://github.com/meteroid-oss/meteroid-go/issues/15)) ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))
* **api:** update the API definitions ([eb2e9c6](https://github.com/meteroid-oss/meteroid-go/commit/eb2e9c6e2f72cb3e4b4220dc53ee695f9a19f905))

## [0.30.1](https://github.com/meteroid-oss/meteroid-go/compare/v0.30.0...v0.30.1) (2026-10-16)


### Bug Fixes

* **api:** update SDKs to meteroid 0.1.0 ([#13](https://github.com/meteroid-oss/meteroid-go/issues/13)) ([46c89ca](https://github.com/meteroid-oss/meteroid-go/commit/46c89ca3d980d62ecf004f4aa63ae5d62406033e))

## [0.30.0](https://github.com/meteroid-oss/meteroid-go/compare/v0.29.0...v0.30.0) (2026-10-09)


### ⚠ BREAKING CHANGES

* **api:** update SDKs to meteroid 0.1.0 ([#11](https://github.com/meteroid-oss/meteroid-go/issues/11))
* **api:** `POST /api/v1/events/ingest`: the `events/items/timestamp` request property `type/format` changed from `string` to `string, null/date-time`

### Features

* **api:** `POST /api/v1/events/ingest`: the `events/items/timestamp` request property `type/format` changed from `string` to `string, null/date-time` ([31e6cf3](https://github.com/meteroid-oss/meteroid-go/commit/31e6cf340264681c09071671fd2c2ffc8a3f09c7))
* **api:** add `DELETE /api/v1/webhooks/endpoints/{endpoint_id}` ([31e6cf3](https://github.com/meteroid-oss/meteroid-go/commit/31e6cf340264681c09071671fd2c2ffc8a3f09c7))
* **api:** update `GET /api/v1/plans` and 1029 more ([31e6cf3](https://github.com/meteroid-oss/meteroid-go/commit/31e6cf340264681c09071671fd2c2ffc8a3f09c7))
* **api:** update SDKs to meteroid 0.1.0 ([#11](https://github.com/meteroid-oss/meteroid-go/issues/11)) ([31e6cf3](https://github.com/meteroid-oss/meteroid-go/commit/31e6cf340264681c09071671fd2c2ffc8a3f09c7))

## [0.29.0](https://github.com/meteroid-oss/meteroid-go/compare/v0.28.0...v0.29.0) (2026-10-08)


### ⚠ BREAKING CHANGES

* **api:** update SDKs to meteroid 0.1.0 ([#9](https://github.com/meteroid-oss/meteroid-go/issues/9))

### Features

* **api:** update SDKs to meteroid 0.1.0 ([#9](https://github.com/meteroid-oss/meteroid-go/issues/9)) ([71ee10a](https://github.com/meteroid-oss/meteroid-go/commit/71ee10a371f75c0053f43ac388b5881bad2755b2))

## [0.28.0](https://github.com/meteroid-oss/meteroid-go/compare/v0.27.1...v0.28.0) (2026-10-07)


### ⚠ BREAKING CHANGES

* **api:** update SDKs to meteroid 0.1.0 ([#7](https://github.com/meteroid-oss/meteroid-go/issues/7))

### Features

* **api:** update SDKs to meteroid 0.1.0 ([#7](https://github.com/meteroid-oss/meteroid-go/issues/7)) ([be84478](https://github.com/meteroid-oss/meteroid-go/commit/be844783236237808864364cb901a10bcf6d6ab7))

## [0.27.1](https://github.com/meteroid-oss/meteroid-go/compare/v0.27.0...v0.27.1) (2026-10-06)


### Bug Fixes

* **api:** update SDKs to meteroid 0.1.0 ([#3](https://github.com/meteroid-oss/meteroid-go/issues/3)) ([2b85746](https://github.com/meteroid-oss/meteroid-go/commit/2b8574641617caad379ae4c79b9cc3e9f24c6953))

## [0.27.0](https://github.com/meteroid-oss/meteroid-go/compare/v0.1.0...v0.27.0) (2026-10-06)


### Features

* **api:** update SDKs to meteroid 0.1.0 ([#1](https://github.com/meteroid-oss/meteroid-go/issues/1)) ([8513e6e](https://github.com/meteroid-oss/meteroid-go/commit/8513e6e43f931bad05fe55cbdef812b83c9535ad))
