https://github.com/user-attachments/assets/77652547-f48b-4959-8655-370f4add9390

※マネキンは定期的に位置を出力、ジャンプしたときにも出力。また、青いキューブからはコリジョンがヒットした際に出力するようにしている。

# 実現したいこと
debugLogのような表現をインゲームでビジュアルとして利用

映像としてよく（？）見かける、コンソール画面を文字列がブワーッと流れる感じをやりたかった

# できること

- 機能１：BPに１ノード追加するだけで利用できる
- 機能２：異なるBPから共通のUMGに表示できる
- 機能２：BPから1行ごとにテキストをLogとして表示できる
- 機能３：BPから直近追加したLogの末尾にテキストを追加できる
- 機能４：Logは一定量で削除される

# 使い方

1. プラグインをインポート
2. BP_InGameLoggerをレベル上に配置
3. 適当なActorからIGL_AddLineやIGL_AddTextToLineを呼び出し、引数に文字列を渡す
  - 実装例：Level Blueprintなどに以下のようなノード設置してみてください
  - <img width="726" height="463" alt="image" src="https://github.com/user-attachments/assets/8a0a6af8-ba87-4ca5-bc7a-5de2406972fa" />

    
        

# 環境
UE5.5.4で作成。他のバージョンでは未確認
