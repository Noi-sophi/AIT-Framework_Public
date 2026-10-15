---
doc: canon
aspect: meta
status: frozen
rev: 0.4.0
---

# AITF Core

## 0. 位置づけ

本稿は、AITF全体で維持する最小限の基礎前提・規定・分析規約を定める。

Coreでは、以下を扱う。

- `world`

- `agent`

- agentによる取り扱いにおける有限性

- `physical / agent / social / meta` のaspect


形式・意味・記述・参照・状態・遷移・具体的な操作などの詳細は、本稿では定めない。

本稿の設計理由、背景、代替案、検討結果については、[AITF_Core_Support](../SUPPORT/AITF_Core_Support.md) を参照する。

---

## 1. `world`

AITFは、`world` を基礎概念として前提する。

`world` は、AITFが扱う事柄が成立し、agentもそれに関与する現実を指す。

Coreでは、`world` の完全な存在論的定義を与えない。

---

## 2. `agent`

AITFは、`agent` を基礎概念として認める。

agentは、`world` との関係において、`world` を扱いうる主体を指す。

Coreでは、agentの必要十分条件や内部構造を定めない。

---

## 3. 有限性

agentによる事柄の取り扱いには、区別・情報・資源・アクセスなどに関する制約が現れうる。

AITFでは、取り扱いにこのような制約をもつagentを、有限agentとして扱う。

有限性は、agent単独の絶対的属性ではなく、agentによる取り扱いと、その対象・条件との関係において現れる。

Coreでは、agentと有限agentを同一視せず、すべてのagentが有限であるとは規定しない。

有限agentであることは、個々の取り扱いが常に不完全であることを意味しない。

有限性が現れる主要な制約軸として、以下を扱う。

- 区別

- 情報

- 資源

- アクセス


Coreでは、これらを有限agentの必要十分な四条件として固定しない。

---

## 4. aspect

aspectは、分析において区別して扱う条件・関係・構造の種類を指定するindexである。

AITFでは、次の四つのaspectを用いる。

- `physical`

- `agent`

- `social`

- `meta`


aspectは、分析対象を排他的な種類へ分類するためのものではない。

同一の事柄について、複数のaspectを適用できる。

Coreでは、aspect間に以下を仮定しない。

- 上位・下位の順序

- 包含関係

- 還元関係

- 一般的な優先順位


また、aspect index自体は、`world` との包含・排他関係によって位置づけない。

### 4.1 `physical`

`physical` は、物理的な条件・相互作用・制約に関わるaspectである。

### 4.2 `agent`

`agent` は、agentに局所的な条件・相互作用・差異に関わるaspectである。

agentそのものを、このaspectから導出しない。

### 4.3 `social`

`social` は、複数agent間の関係、共有された条件、制度的・社会的構造に関わるaspectである。

### 4.4 `meta`

`meta` は、形式・記述・推論その他の形式的構造に関わるaspectである。

### 4.5 `meta` の非対称性

四aspectは共通の分析indexとして用いるが、その意味的性質が対称であることを要求しない。

特に `meta` は形式的・記述的構造に関わり、そのような構造自身にも適用できる。

---

## 5. 境界

Coreでは、以下を定めない。

- token / form

- meaning

- description / interpretation

- object / representation / reference

- state / transition

- agent内部のモジュールや処理構造

- aspectを指定・適用・操作する具体的方法

- Standard上の操作


state / transitionを、Coreでは `world` の構成要素として仮定しない。
