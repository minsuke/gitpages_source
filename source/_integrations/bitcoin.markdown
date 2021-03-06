---
title: 비트코인(Bitcoin)
description: Instructions on how to integrate Bitcoin data within Home Assistant.
logo: bitcoin.png
ha_category:
  - Finance
ha_release: pre 0.7
ha_iot_class: Cloud Polling
ha_codeowners:
  - '@fabaff'
---

비트 코인 센서 플랫폼은 [Bitcoin](https://bitcoin.org) 네트워크에 대한 다양한 세부 사항을 표시합니다.

비트 코인 센서를 설치에 추가하려면, 사용 가능한 디스플레이 옵션을 `configuration.yaml` 파일에 추가하십시오 :

```yaml
# Example configuration.yaml entry
sensor:
  - platform: bitcoin
    display_options:
      - exchangerate
      - trade_volume_btc
```

{% configuration %}
currency:
  description: The currency to exchange to, e.g., CHF, USD, EUR, etc.
  required: false
  type: string
  default: USD
display_options:
  description: Options to display in the frontend.
  required: true
  type: list
  keys:
    exchangerate:
      description: Exchange rate of 1 BTC
    trade_volume_btc:
      description: Trade volume
    miners_revenue_usd:
      description: Miners revenue
    btc_mined:
      description: BTC mined
    trade_volume_usd:
      description: Trade volume in USD
    difficulty:
      description: Difficulty
    minutes_between_blocks:
      description: Time between blocks in minutes
    number_of_transactions:
      description: Number of transactions
    hash_rate:
      description: Hash rate in PH/s
    timestamp:
      description: Timestamp
    mined_blocks:
      description: Mined Blocks
    blocks_size:
      description: Block size
    total_fees_btc:
      description: Total fees in BTC
    total_btc_sent:
      description: Total sent in BTC
    estimated_btc_sent:
      description: Estimated sent in BTC
    total_btc:
      description: Total of BTC
    total_blocks:
      description: Total Blocks
    next_retarget:
      description: Next retarget
    estimated_transaction_volume_usd:
      description: Estimated transaction volume in BTC
    miners_revenue_btc:
      description: Miners revenue in BTC
    market_price_usd:
      description: Market price in USD
{% endconfiguration %}
