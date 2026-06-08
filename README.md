# fizz-prompt-builder

**Fizz** (AITuber system in [Almide](https://github.com/almide/almide)) — §3 brain 部品。

persona system prompt + recall preamble + few-shot + 会話履歴 + 着弾コメントを
LLM の messages 列に組み立てる。出力は [fizz-llm-client](https://github.com/Aid-On/fizz-llm-client)
の `Message` 列 (= そのまま `call_with` に渡せる)。

組み立て順: system(+recall) → few-shot(user/assistant 交互) → history → 今回の user コメント。
入力はプリミティブで受け、persona/history/retriever への直接依存を持たない (疎結合)。

## Install
```toml
[dependencies]
fizz_prompt_builder = { git = "https://github.com/Aid-On/fizz-prompt-builder", tag = "v0.1.0" }
```

## Tests
```bash
almide test
```
