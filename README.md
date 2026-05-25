# Nuvei (nuvei)

Nuvei is a global payment technology company headquartered in Montreal, Canada, offering a single platform for online card acquiring, alternative payment methods (700+ APMs), payouts, currency management across 150+ currencies, fraud/risk, and payment orchestration. Nuvei serves merchants in 200+ markets with local acquiring in 52 markets across eCommerce, iGaming, sports betting, travel, retail, B2B, and financial services. Originally listed on Nasdaq and TSX as NVEI, Nuvei was taken private by Advent International in 2024.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/nuvei/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Payments, Payment Processing, Payment Gateway, Acquiring, Payouts, Alternative Payment Methods, Fraud, Risk, Currency Conversion, iGaming, eCommerce, FinTech

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## Base URLs

| Environment | URL |
|---|---|
| Production | `https://secure.safecharge.com/ppp/api/v1/` |
| Sandbox | `https://ppp-test.nuvei.com/ppp/api/v1/` |

Authentication uses a SHA-256 checksum computed over an ordered concatenation of `merchantId`, `merchantSiteId`, `clientRequestId`, `amount`, `currency`, `timeStamp`, and the `merchantSecretKey`.

## APIs

### Nuvei Payments API
Server-to-server REST API for processing card and APM transactions. Includes `payment`, `settleTransaction`, `voidTransaction`, `refundTransaction`, and `getPaymentStatus`.

- [Documentation](https://docs.nuvei.com/documentation/integration/server-to-server/server-to-server-introduction/)
- [OpenAPI](openapi/nuvei-payments-api-openapi.yml)
- [JSON Schema — Payment](json-schema/nuvei-payment-schema.json)
- [JSON Schema — Transaction](json-schema/nuvei-transaction-schema.json)
- [Naftiko Capability — Payments](capabilities/payments-payments.yaml)
- [Naftiko Capability — Refunds/Voids/Settles](capabilities/payments-refunds.yaml)

### Nuvei Session API
`getSessionToken` issues a short-lived sessionToken used by the REST API and Web SDK.

- [OpenAPI](openapi/nuvei-session-api-openapi.yml)
- [Naftiko Capability — Sessions](capabilities/session-sessions.yaml)

### Nuvei Order API
Creates and updates orders before payment via `openOrder` and `updateOrder`.

- [OpenAPI](openapi/nuvei-order-api-openapi.yml)
- [Naftiko Capability — Orders](capabilities/orders-orders.yaml)

### Nuvei Payouts API
Push funds to consumers and counterparties via card, bank account, and local APMs. Includes `payout` and `accountCapture`.

- [OpenAPI](openapi/nuvei-payouts-api-openapi.yml)
- [Naftiko Capability — Payouts](capabilities/payouts-payouts.yaml)

### Nuvei User Payment Options API
Manage stored payment instruments (UPOs) for cards and APMs.

- [OpenAPI](openapi/nuvei-user-payment-options-api-openapi.yml)
- [Naftiko Capability — Tokens](capabilities/user-payment-options-tokens.yaml)

### Nuvei Merchant Configuration API
Look up supported countries and payment methods per country.

- [OpenAPI](openapi/nuvei-merchant-config-api-openapi.yml)
- [Naftiko Capability — Payment Methods](capabilities/merchant-config-payment-methods.yaml)

### Nuvei 3DS API
3-D Secure 2 authentication (`getCard3DDetails`, `authenticate3d`) for PSD2 SCA.

- [OpenAPI](openapi/nuvei-3ds-api-openapi.yml)
- [Naftiko Capability — 3DS](capabilities/three-ds-authentication.yaml)

### Nuvei DCC API
Dynamic Currency Conversion quotes (`getDccDetails`).

- [OpenAPI](openapi/nuvei-dcc-api-openapi.yml)
- [Naftiko Capability — DCC](capabilities/dcc-conversions.yaml)

### Nuvei Direct Merchant Notifications (DMN)
Server-to-server webhook delivery for payments, payouts, refunds, voids, settles, and Control Panel events. Payment DMNs are signed via `advanceResponseChecksum`.

- [Documentation](https://docs.nuvei.com/documentation/integration/webhooks/)
- [AsyncAPI](asyncapi/nuvei-dmn-asyncapi.yml)
- [Payment DMN example](examples/nuvei-payment-dmn-example.json)

## Server SDKs

| Language | Repo |
|---|---|
| PHP | [Nuvei/nuvei-server-php](https://github.com/Nuvei/nuvei-server-php) |
| Java | [Nuvei/nuvei-server-java](https://github.com/Nuvei/nuvei-server-java) |
| Java 2.0 | [Nuvei/nuvei-server-java-2.0](https://github.com/Nuvei/nuvei-server-java-2.0) |
| Node.js | [Nuvei/nuvei-server-nodejs](https://github.com/Nuvei/nuvei-server-nodejs) |

## Mobile SDKs

| Platform | Repo |
|---|---|
| iOS | [Nuvei/nuvei-mobile-sdk-ios](https://github.com/Nuvei/nuvei-mobile-sdk-ios) |
| Android | [Nuvei/nuvei-mobile-sdk-android](https://github.com/Nuvei/nuvei-mobile-sdk-android) |
| React Native | [Nuvei/nuvei-react-native-mobile-sdk](https://github.com/Nuvei/nuvei-react-native-mobile-sdk) |
| iOS Cashier Helper | [Nuvei/nuvei-mobile-cashier-helper-ios](https://github.com/Nuvei/nuvei-mobile-cashier-helper-ios) |
| Android Cashier Helper | [Nuvei/nuvei-mobile-cashier-helper-android](https://github.com/Nuvei/nuvei-mobile-cashier-helper-android) |
| Android Cashier Helper (React) | [Nuvei/nuvei-cashier-helper-react-for-android](https://github.com/Nuvei/nuvei-cashier-helper-react-for-android) |
| CocoaPods distribution | [Nuvei/nuvei-mobile-pods](https://github.com/Nuvei/nuvei-mobile-pods) |
| Maven distribution | [Nuvei/nuvei-maven-android](https://github.com/Nuvei/nuvei-maven-android) |

## eCommerce Plugins

- [Magento 2](https://github.com/Nuvei/nuvei-plugin-magento-2)
- [WooCommerce](https://github.com/Nuvei/nuvei-plugin-woocommerce)
- [PrestaShop](https://github.com/Nuvei/nuvei-plugin-prestashop)
- [OpenCart 3](https://github.com/Nuvei/nuvei-plugin-opencart-3) / [OpenCart 4](https://github.com/Nuvei/nuvei-plugin-opencart-4)
- [Shopware 5](https://github.com/Nuvei/nuvei-plugin-shopware-5) / [Shopware 6](https://github.com/Nuvei/nuvei-plugin-shopware-6)
- [Salesforce Commerce Cloud](https://github.com/Nuvei/nuvei-plugin-salesforce-commerce-cloud)
- [SAP Commerce](https://github.com/Nuvei/nuvei-plugin-sap-commerce)
- [commercetools Backend](https://github.com/Nuvei/nuvei-plugin-commerce-tools-backend) / [commercetools Frontend](https://github.com/Nuvei/nuvei-plugin-commerce-tools-frontend)

## Commercial Surface

- [Plans / Pricing](plans/nuvei-plans-pricing.yml)
- [Rate Limits](rate-limits/nuvei-rate-limits.yml)
- [FinOps Mapping](finops/nuvei-finops.yml)

## Semantics and Conventions

- [Vocabulary](vocabulary/nuvei-vocabulary.yml)
- [JSON-LD Context](json-ld/nuvei-context.jsonld)
- [JSON Structure — Payment](json-structure/nuvei-payment-structure.json)
- [Spectral Ruleset](rules/nuvei-rules.yml)

## Examples

- [Open Order](examples/nuvei-open-order-example.json)
- [Payment](examples/nuvei-payment-example.json)
- [Refund](examples/nuvei-refund-example.json)
- [Payment DMN](examples/nuvei-payment-dmn-example.json)
