# mizdra/renovate-config-mizdra

Shareable Renovate Config for @mizdra

## Usage

以下のファイルを `renovate.json` という名前でリポジトリ直下に置くと、

`mizdra/renovate-config-mizdra` は一般的なプロジェクト向けの preset である [`default.json5`](https://github.com/mizdra/renovate-config-mizdra/blob/main/default.json5) と、その他いくつかの optional な preset を提供しています。基本的に `default.json5` を extends して、必要に応じて optional な preset を extends するような運用を想定しています。

`default.json5` を extends するには、ご利用のプロジェクトのルートに `renovate.json` を作成し、以下のように記述します。

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>mizdra/renovate-config-mizdra:default.json5"]
}
```

続けて optional な preset を extends するには、`renovate.json` を以下のように記述します。

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>mizdra/renovate-config-mizdra:default.json5", "github>mizdra/renovate-config-mizdra:+lib.json5"]
}
```

## Optional presets

### [`+lib`](https://github.com/mizdra/renovate-config-mizdra/blob/main/+lib.json5)

ライブラリ向けの preset です。`mizdra/renovate-config-mizdra` はデフォルトでアプリケーション向けに設定がカスタマイズされているため、ライブラリで利用する場合はこの preset を継承するようにしてください。

## LICENSE

This project is written with some modified parts of [hatena/renovate-config](https://github.com/hatena/renovate-config) and [cybozu/renovate-config](https://github.com/cybozu/renovate-config). The project is licensed under the MIT License.
