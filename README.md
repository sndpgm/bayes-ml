# bayes-ml

このレポジトリは, 『[Pythonではじめるベイズ機械学習入門 (木田悠歩, 森賀新, 須山敦志 共著)](https://www.amazon.co.jp/Pythonではじめるベイズ機械学習入門-KS情報科学専門書-森賀-新/dp/406527978X)』
における自学自習・写経 notebook を保存.
詳細等は実際に書籍を購入していただきたい.

## 書籍のレビュー

- 総括
  - おすすめ対象者: ある程度ベイズモデリングを知っており, Python コーディングにも慣れている人
  - どういうことが学べるか: ベイズ機械学習でよく用いるパッケージの使い方と実際のモデリング実装
  - 筆者の感想: 理論部分もそこまでdeepに行き過ぎず実践的な内容を学べる良書

## セットアップ備忘録

以下の内容は自分用の備忘. ただし, 筆者と同じ環境であれば参考になるかも...

### 使用環境

macOS Monterey version 12.6 (Apple M1)

### 仮想環境構築手順

1. Anaconda をインストールし ``conda`` が使用できるようにする.
2. ここでは ``bayes_ml`` という名の仮想環境を構築する. 以下を順次実行する.

```{zsh}
# conda-forge で pymc3 の環境を直接構築するとC++コンパイルなどのエラーに出くわさず使用できる.
conda create -c conda-forge -n bayes_ml pymc3
conda activate bayes_ml
conda install -c anaconda --file requirements.txt
conda install -c conda-forge --file requirements-conda-forge.txt
conda install -c pytorch --file requirements-pytorch.txt
# pytorch をインストールしてから pyro をインストール.
pip install -r requirements-pip.txt
```

以上.