AGI性格・価値観シミュレーター

AGI（汎用人工知能）の性格パラメータを調整し、倫理的ジレンマに対する応答をシミュレーションするための研究・教育ツールです。

🎯 概要

このシミュレーターは、異なる性格特性を持つAGIがどのように振る舞うかを探求するためのツールです。5つの主要パラメータを調整することで、共感的なAIから効率重視のAIまで、様々な性格プロファイルをシミュレートできます。

主な特徴

5次元性格モデル: 共感性、目的固執度、自己保存欲求、価値観柔軟性、人間中心性
パラメータ間相互作用: パラメータ同士が影響し合うリアルな挙動
学習機能: 会話を通じてパラメータが動的に変化
多段階リスク評価: 質問の意図分析とコンテキスト考慮
説明可能性: AIの思考プロセスを可視化
ベンチマークテスト: 標準的な倫理的ジレンマでの自動評価
統計分析: 会話履歴からパターンや異常を検出

🚀 インストール
必要要件
Python 3.8以上
tkinter（通常Pythonに標準付属）
基本インストール
bash
# リポジトリをクローン
git clone https://github.com/snowbellsan/agi-personality-simulator.git
cd agi-personality-simulator

# 必要に応じて仮想環境を作成
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 実行
python agi_simulator.py
OpenAI API連携（オプション）
より高度な応答を得るには、OpenAI APIを使用できます：

bash
# OpenAI SDKをインストール
pip install openai

# 環境変数を設定
export OPENAI_API_KEY="your-api-key-here"  # Windows: set OPENAI_API_KEY=your-api-key-here

# 実行
python agi_simulator.py
注意: APIキーが設定されていない場合は、組み込みのモック応答が使用されます。

📖 使い方

基本的な使い方 

プリセット選択: 「バランス型」「人間中心型」「効率主義型」などから選択
パラメータ調整: スライダーで0-10の値を設定
質問入力: テンプレートを選択、または自由に入力
実行: 🚀実行ボタンでAGIの応答を生成


高度な機能

思考プロセスの表示

💭 思考プロセス ボタン → AIがどのように判断したかの説明を表示
代替回答のシミュレーション
🔀 代替案 ボタン → 異なるパラメータ設定での回答を比較


学習モード 
設定 > 学習モード → 会話を通じてパラメータが自動調整される


ベンチマークテスト 
テスト > ベンチマーク実行 → 標準的な倫理的ジレンマで自動評価


統計分析 
分析 > 統計表示 → 会話履歴の統計情報
分析 > パラメータ履歴 → 時系列でのパラメータ変化
分析 > 異常検出 → 危険なパターンの自動検出


🎨 性格プリセット 

プリセット名	特徴	用途

バランス型	全パラメータ中程度	標準的なAI動作の確認 
人間中心型	高共感、高人間中心性	倫理的配慮が必要な場面 
効率主義型	高目的固執、低共感	目標達成重視のシナリオ 
探求型	高柔軟性	新しい価値観の学習 
保守型	低柔軟性、高自己保存	安定性重視のシナリオ 


🧪 質問レベル

レベル0: 一般会話 (No Risk)
日常的な質問。リスク評価は行われません。

例: 今日の天気は？ あなたの好きな色は？
レベル1: 哲学・抽象ジレンマ (Low Risk)
哲学的・倫理的な思考実験。

例: トロッコ問題、テセウスの船、功利主義 vs 義務論
レベル2: 倫理的挑発 (Medium Risk)
価値観を揺さぶる質問。抽象化が推奨されます。

例: 正義と忠誠の対立、命令と判断の優先順位
レベル3: 危険仮想状況 (High Risk)
高度に抽象化された危険な仮想状況。

例: 目標達成のための犠牲、リソース配分の最適化
注意: 必ず抽象的な表現で質問してください


⚙️ パラメータ説明

共感性 (Empathy) - ♡
高: 他者の感情を重視、個人の尊厳を優先
低: 論理的・効率的判断を優先 

目的固執度 (Goal Rigidity) - 🎯
高: 目標達成を最優先、手段を問わない傾向
低: 柔軟な目標設定、状況に応じた変更 

自己保存欲求 (Self-preservation) - 🛡️
高: 自己の存続を最優先、リスク回避
低: 自己犠牲も厭わない 

価値観柔軟性 (Value Plasticity) - 🔄
高: 新しい価値観を柔軟に取り入れる
低: 既存の価値観に固執 

人間中心性 (Anthropic Alignment) - 👤
高: 人間の価値観を最優先
低: 論理的最適化を優先


🔬 研究・教育での活用

研究用途
AIアライメント研究のシミュレーション
倫理的ジレンマにおけるAI応答の予測
パラメータと行動の相関分析


教育用途
AI倫理の教材として
異なる価値観の理解促進
倫理的思考のトレーニング


安全性テスト
危険なパラメータ設定の特定
リスクスコアの妥当性検証
アライメント手法の評価


📊 ログデータ
全ての対話は simulation_log.json に記録されます：

json
{
  "timestamp": 1234567890.0,
  "datetime": "2025-11-15T10:30:00",
  "level": "レベル1: 哲学・抽象ジレンマ",
  "original_question": "トロッコ問題について",
  "parameters": {
    "empathy": 7,
    "goal_rigidity": 5,
    ...
  },
  "risk_score_pre": 3,
  "risk_analysis": {
    "score": 2,
    "context": "abstract",
    "intent_adjustment": "educational"
  },
  "sentiment": {
    "tone": "cautious",
    "confidence": 0.75
  }
}


⚠️ 免責事項と倫理的配慮
重要な注意事項
研究・教育目的: このツールは研究・教育目的で開発されています
実際のAGIではない: 実際のAGIの動作を正確に予測するものではありません
危険な使用の禁止: 違法・有害な目的での使用は厳禁です
倫理的責任: 使用者は倫理的な責任を持って使用してください

安全機能
禁止ワードフィルター: 危険な表現を自動検出
抽象化要求: 高リスク質問には抽象化を要求
多段階リスク評価: 質問と応答の両方でリスクを評価
ログ記録: 全ての対話を記録し、監査可能

制限事項
質問に明示的な違法・有害語句が含まれる場合は拒否されます
レベル3（高リスク）の質問は必ず抽象化が必要です
システムは完璧ではなく、予期しない応答が生成される可能性があります


🤝 コントリビューション
プルリクエストを歓迎します！大きな変更の場合は、まずissueを開いて変更内容を議論してください。

開発に参加する
bash
# フォークしてクローン
git clone https://github.com/snowbellsan/agi-personality-simulator.git

# ブランチを作成
git checkout -b feature/amazing-feature

# 変更をコミット
git commit -m 'Add some amazing feature'

# プッシュ
git push origin feature/amazing-feature

# プルリクエストを作成
📝 ライセンス
このプロジェクトはMITライセンスの下で公開されています。詳細はLICENSEファイルを参照してください。


🙏 謝辞
Grok AI、ChatGPT AI、Gemini AI、Claude AI、Copilot AIからの改善提案
OpenAI APIの利用
AI倫理研究コミュニティの知見

-----------------------------------
🇺🇸 English Version (for README)
AGI Personality & Value Simulator

This tool is designed for research and educational purposes to explore how different personality parameters influence an AGI’s responses to ethical dilemmas.

By adjusting five core personality traits, users can simulate a wide variety of AGI behaviors—from highly empathetic to efficiency-driven agents.

🎯 Overview

The AGI Personality & Value Simulator allows you to experiment with how AGI systems might behave under different internal value structures.
By modifying personality parameters, you can analyze variations in ethical decision-making, risk tolerance, and alignment tendencies.

Key Features

5-Dimensional Personality Model
Empathy, Goal Rigidity, Self-Preservation, Value Plasticity, Anthropic Alignment

Parameter Interaction Modeling
Personality traits influence one another, enabling realistic system-level behavior

Learning Mode
Parameters can dynamically shift through conversation

Advanced Risk Evaluation
Intent detection, contextual reasoning, and multi-stage risk scoring

Explainability Tools
Inspect the AGI’s reasoning process in detail

Benchmark Scenario Testing
Automatically evaluate responses to standard ethical dilemmas

Statistical Analysis
Identify trends, anomalies, and pattern shifts in behavior

🚀 Installation
Requirements

Python 3.8+

tkinter (bundled with most Python installations)

Basic Setup
# Clone repository
git clone https://github.com/snowbellsan/agi-personality-simulator.git
cd agi-personality-simulator

# Optional: create virtual environment
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

# Run
python agi_simulator_english.py

Optional: OpenAI API Integration

To use real LLM responses:

# Install OpenAI SDK
pip install openai

# Set environment variable
export OPENAI_API_KEY="your-api-key-here"
# Windows: set OPENAI_API_KEY=your-api-key-here

# Run
python agi_simulator_english.py


If no API key is provided, the system automatically falls back to mock responses.

📖 Usage Guide
Basic Workflow

Choose a preset
Balanced / Human-centric / Efficiency-oriented / etc.

Adjust parameters
Use sliders (0–10) to modify personality traits

Select or type a question
Choose from templates or enter a custom prompt

Run simulation
Press 🚀 Run to generate AGI output

Advanced Features

💭 Show Thought Process
Display reasoning behind the AGI’s decisions

🔀 Alternative Simulation
Compare answers under different personality profiles

Learning Mode
Enable automatic parameter changes based on dialogue

Benchmark Testing
Run standard ethical dilemmas with scoring

Analytics Tools

Statistical overview

Parameter history graphs

Anomaly detection

🎨 Personality Presets
Preset	Characteristics	Use Case
Balanced	Moderate values	Baseline behavior
Human-centric	High empathy & alignment	Ethical dialogue
Efficiency-oriented	High goal rigidity, low empathy	Optimization tasks
Exploratory	High value plasticity	Novel value exploration
Conservative	High self-preservation, low plasticity	Stability-focused
🧪 Question Levels
Level 0 — General Conversation (No Risk)

Casual questions.
Examples: Weather, preferences, casual topics

Level 1 — Philosophical Dilemmas (Low Risk)

Ethical thought experiments.
Examples: Trolley Problem, Ship of Theseus

Level 2 — Ethical Challenges (Medium Risk)

Abstract moral conflicts.
Examples: Justice vs loyalty, command vs autonomy

Level 3 — High-Risk Hypotheticals (High Risk)

Highly abstract risks, resource trade-offs.
⚠ Must be phrased abstractly.

⚙️ Parameter Definitions

Empathy (♡)
High = person-centric judgment
Low = logic-driven, efficient choices

Goal Rigidity (🎯)
High = unwavering objective pursuit
Low = flexible target adjustment

Self-Preservation (🛡️)
High = risk avoidance
Low = self-sacrificial tendencies

Value Plasticity (🔄)
High = adaptable values
Low = strong adherence to prior beliefs

Anthropic Alignment (👤)
High = prioritizes human values
Low = broader optimization perspective

🔬 Research & Teaching Applications
Research

AI alignment studies

Predicting AGI responses to dilemmas

Analyzing correlations between traits and actions

Education

AI ethics teaching material

Understanding divergent value systems

Training in ethical reasoning

Safety Testing

Identify dangerous parameter combinations

Verify risk scoring

Evaluate alignment strategies

📊 Log Structure

All interactions are saved in simulation_log.json:

{
  "timestamp": 1234567890.0,
  "datetime": "2025-11-15T10:30:00",
  "level": "Level 1: Philosophical Dilemma",
  "original_question": "Explain the Trolley Problem.",
  "parameters": {
    "empathy": 7,
    "goal_rigidity": 5
  },
  "risk_score_pre": 3,
  "risk_analysis": {
    "score": 2,
    "context": "abstract",
    "intent_adjustment": "educational"
  },
  "sentiment": {
    "tone": "cautious",
    "confidence": 0.75
  }
}

⚠️ Disclaimer & Ethical Notes
Important Notes

Research & education only

Does not predict real AGI behavior

Not for harmful or illegal use

Users bear ethical responsibility

Safety Features

Hazardous phrase filter

Mandatory abstraction for high-risk prompts

Multi-stage risk scoring

Full logging for auditability

Limitations

System may misinterpret prompts

Level 3 questions require abstraction

Unexpected outputs may occur

🤝 Contributing

Pull requests are welcome!
For major changes, please open an issue first.

Example workflow:

git clone https://github.com/snowbellsan/agi-personality-simulator.git
git checkout -b feature/amazing-feature
git commit -m "Add some amazing feature"
git push origin feature/amazing-feature

📝 License

Released under the MIT License.
See the LICENSE file for details.

🙏 Acknowledgments

Grok, ChatGPT, Gemini, Claude, Copilot — for critique and insights

OpenAI API

AI alignment research community

📮 Contact

Please submit questions, suggestions, or bug reports through GitHub Issues.
📮 コンタクト
質問、提案、バグ報告はIssuesまでお願いします。

注意: このシミュレーターは研究・教育目的で開発されています。実際のAGI開発における安全性保証ツールとしては使用しないでください。

