**简体中文** · [English](README.en.md)

# ![freqtrade](https://raw.githubusercontent.com/freqtrade/freqtrade/develop/docs/assets/freqtrade_poweredby.svg)

[![Freqtrade CI](https://github.com/freqtrade/freqtrade/actions/workflows/ci.yml/badge.svg?branch=develop)](https://github.com/freqtrade/freqtrade/actions/workflows/ci.yml)
[![DOI](https://joss.theoj.org/papers/10.21105/joss.04864/status.svg)](https://doi.org/10.21105/joss.04864)
[![codecov](https://codecov.io/gh/freqtrade/freqtrade/branch/develop/graph/badge.svg?token=AD5BG3ATKI)](https://codecov.io/gh/freqtrade/freqtrade)
[![Documentation](https://readthedocs.org/projects/freqtrade/badge/)](https://www.freqtrade.io)
[![Discord Server](https://img.shields.io/badge/Freqtrade_Discord-4E4E4E?logo=discord)](https://discord.gg/p7nuUNVfP7)

Freqtrade 是一款用 Python 编写的免费开源加密货币交易机器人。它旨在支持所有主流交易所，并可通过 Telegram 或 WebUI 进行控制。它包含回测、绘图和资金管理工具，还支持通过机器学习进行策略优化。

![freqtrade](https://raw.githubusercontent.com/freqtrade/freqtrade/develop/docs/assets/freqtrade-screenshot.png)

## 免责声明

本软件仅供教育用途。请不要拿你输不起的钱去冒险。使用本软件的风险由你自行承担。作者及所有关联方对你的交易结果不承担任何责任。

请始终先以模拟运行（Dry-Run）模式运行交易机器人，在你了解它的工作原理以及预期的盈亏之前，不要投入真金白银。

我们强烈建议你具备编程和 Python 知识。不要犹豫，去阅读源代码，理解这个机器人的运作机制。

## 支持的交易所

请阅读[各交易所的特别说明](https://www.freqtrade.io/en/stable/exchanges/)，了解每个交易所可能需要的特殊配置。

### 支持的现货交易所

- [X] [Binance](https://www.binance.com/)
- [X] [BingX](https://bingx.com/invite/0EM9RX)
- [X] [Bitget](https://www.bitget.com/)
- [X] [Bybit EU](https://bybit.eu/)
- [X] [Bybit](https://bybit.com/)
- [X] [Gate EU](https://www.gate.com/en-eu)
- [X] [Gate](https://www.gate.com/ref/6266643)
- [X] [HTX](https://www.htx.com/)
- [X] [Hyperliquid](https://hyperliquid.xyz/)（去中心化交易所，即 DEX）
- [X] [Kraken](https://kraken.com/)
- [X] [MyOKX](https://okx.com/) (OKX EEA)
- [X] [OKX](https://okx.com/)
- [ ] [可能还有很多其他交易所](https://github.com/ccxt/ccxt/)。_（我们无法保证它们能正常工作）_

### 支持的合约交易所

- [X] [Binance](https://www.binance.com/)
- [X] [Bitget](https://www.bitget.com/)
- [X] [Bybit](https://bybit.com/)
- [X] [Gate](https://www.gate.com/ref/6266643)
- [X] [Hyperliquid](https://hyperliquid.xyz/)（去中心化交易所，即 DEX）
- [X] [Kraken](https://www.kraken.com/features/futures)
- [X] [OKX](https://okx.com/)

开始之前，请务必阅读[各交易所的特别说明](https://www.freqtrade.io/en/stable/exchanges/)以及[杠杆交易](https://www.freqtrade.io/en/stable/leverage/)文档。

### 社区测试

经社区确认可正常使用的交易所：

- [X] [Bitvavo](https://bitvavo.com/)
- [X] [Kucoin](https://www.kucoin.com/)

## 文档

我们建议你阅读机器人的文档，以确保你理解它的工作方式。

完整文档请访问 [freqtrade 官网](https://www.freqtrade.io)。

## 功能特性

- [x] **基于 Python 3.12+**：可在任何操作系统上运行——Windows、macOS 和 Linux。
- [x] **持久化**：通过 sqlite 实现数据持久化。
- [x] **模拟运行（Dry-run）**：无需花钱即可运行机器人。
- [x] **回测**：对你的买入/卖出策略进行模拟。
- [x] **通过机器学习优化策略**：使用机器学习，基于真实交易所数据优化你的买入/卖出策略参数。
- [X] **自适应预测建模**：使用 FreqAI 构建智能策略，通过自适应机器学习方法根据市场自我训练。[了解更多](https://www.freqtrade.io/en/stable/freqai/)
- [x] **加密货币白名单**：选择你想交易的加密货币，或使用动态白名单。
- [x] **加密货币黑名单**：选择你想避开的加密货币。
- [x] **内置 WebUI**：内置 Web 界面，用于管理你的机器人。
- [x] **可通过 Telegram 管理**：使用 Telegram 管理机器人。
- [x] **以法币显示盈亏**：以法定货币显示你的盈亏。
- [x] **业绩状态报告**：提供当前交易的业绩状态。

## 快速开始

如何快速上手，请参阅 [Docker 快速开始文档](https://www.freqtrade.io/en/stable/docker_quickstart/)。

其他（原生）安装方式，请参阅[安装文档页面](https://www.freqtrade.io/en/stable/installation/)。

## 基本用法

### 机器人命令

```
usage: freqtrade [-h] [-V]
                 {trade,create-userdir,new-config,show-config,new-strategy,download-data,convert-data,convert-trade-data,trades-to-ohlcv,list-data,backtesting,backtesting-show,backtesting-analysis,edge,hyperopt,hyperopt-list,hyperopt-show,list-exchanges,list-markets,list-pairs,list-strategies,list-hyperoptloss,list-freqaimodels,list-timeframes,show-trades,test-pairlist,convert-db,install-ui,plot-dataframe,plot-profit,webserver,strategy-updater,lookahead-analysis,recursive-analysis}
                 ...

Free, open source crypto trading bot

positional arguments:
  {trade,create-userdir,new-config,show-config,new-strategy,download-data,convert-data,convert-trade-data,trades-to-ohlcv,list-data,backtesting,backtesting-show,backtesting-analysis,edge,hyperopt,hyperopt-list,hyperopt-show,list-exchanges,list-markets,list-pairs,list-strategies,list-hyperoptloss,list-freqaimodels,list-timeframes,show-trades,test-pairlist,convert-db,install-ui,plot-dataframe,plot-profit,webserver,strategy-updater,lookahead-analysis,recursive-analysis}
    trade               Trade module.
    create-userdir      Create user-data directory.
    new-config          Create new config
    show-config         Show resolved config
    new-strategy        Create new strategy
    download-data       Download backtesting data.
    convert-data        Convert candle (OHLCV) data from one format to
                        another.
    convert-trade-data  Convert trade data from one format to another.
    trades-to-ohlcv     Convert trade data to OHLCV data.
    list-data           List downloaded data.
    backtesting         Backtesting module.
    backtesting-show    Show past Backtest results
    backtesting-analysis
                        Backtest Analysis module.
    hyperopt            Hyperopt module.
    hyperopt-list       List Hyperopt results
    hyperopt-show       Show details of Hyperopt results
    list-exchanges      Print available exchanges.
    list-markets        Print markets on exchange.
    list-pairs          Print pairs on exchange.
    list-strategies     Print available strategies.
    list-hyperoptloss   Print available hyperopt loss functions.
    list-freqaimodels   Print available freqAI models.
    list-timeframes     Print available timeframes for the exchange.
    show-trades         Show trades.
    test-pairlist       Test your pairlist configuration.
    convert-db          Migrate database to different system
    install-ui          Install FreqUI
    plot-dataframe      Plot candles with indicators.
    plot-profit         Generate plot showing profits.
    webserver           Webserver module.
    strategy-updater    updates outdated strategy files to the current version
    lookahead-analysis  Check for potential look ahead bias.
    recursive-analysis  Check for potential recursive formula issue.

options:
  -h, --help            show this help message and exit
  -V, --version         show program's version number and exit
```

### Telegram RPC 命令

Telegram 不是必需的，但它是控制机器人的好方式。更多细节和完整命令列表请参阅[文档](https://www.freqtrade.io/en/stable/telegram-usage/)。

- `/start`：启动交易。
- `/stop`：停止交易。
- `/stopentry`：停止开新仓。
- `/status <trade_id>|[table]`：列出所有或指定的未平仓交易。
- `/profit [<n>]`：列出最近 n 天所有已完成交易的累计利润。
- `/profit_long [<n>]`：列出最近 n 天所有已完成多头交易的累计利润。
- `/profit_short [<n>]`：列出最近 n 天所有已完成空头交易的累计利润。
- `/forceexit <trade_id>|all`：立即平掉指定交易（忽略 `minimum_roi`）。
- `/fx <trade_id>|all`：`/forceexit` 的别名
- `/performance`：按交易对分组显示每笔已完成交易的业绩
- `/balance`：按币种显示账户余额。
- `/daily <n>`：显示最近 n 天每天的盈亏。
- `/help`：显示帮助信息。
- `/version`：显示版本。


## 开发分支

本项目目前主要设置了以下分支：

- `develop` - 该分支经常有新功能，但也可能包含不兼容的变更。我们会尽力保持该分支的稳定。
- `stable` - 该分支包含最新的稳定版本，通常经过了充分测试。
- `feat/*` - 这些是正在大量开发中的功能分支。除非你想测试某个特定功能，否则请不要使用它们。

## 支持

### 帮助 / Discord

对于文档未涵盖的任何问题、想进一步了解机器人，或者只是想与志同道合的人交流，欢迎加入 Freqtrade [Discord 服务器](https://discord.gg/p7nuUNVfP7)。

### [Bug / 问题](https://github.com/freqtrade/freqtrade/issues?q=is%3Aissue)

如果你发现了机器人的 bug，请先
[搜索 issue 列表](https://github.com/freqtrade/freqtrade/issues?q=is%3Aissue)。
如果还没有人报告过，请
[创建新的 issue](https://github.com/freqtrade/freqtrade/issues/new/choose)，
并遵循模板指引，以便团队尽快为你提供帮助。

对于每一个创建的 [issue](https://github.com/freqtrade/freqtrade/issues/new/choose)，请及时跟进，在问题得到解决时标注满意或提醒关闭 issue。

--遵守 GitHub 的[社区准则](https://docs.github.com/en/site-policy/github-terms/github-community-code-of-conduct)--

### [功能请求](https://github.com/freqtrade/freqtrade/labels/enhancement)

你有改进机器人的好点子想分享吗？请先搜索该功能是否
[已经讨论过](https://github.com/freqtrade/freqtrade/labels/enhancement)。
如果还没有人提出过，请
[创建新的请求](https://github.com/freqtrade/freqtrade/issues/new/choose)，
并遵循模板指引，以免它淹没在 bug 报告中。

### [Pull Request](https://github.com/freqtrade/freqtrade/pulls)

觉得机器人缺少某个功能？欢迎提交 pull request！

在提交 pull request 之前，请阅读
[贡献指南](https://github.com/freqtrade/freqtrade/blob/develop/CONTRIBUTING.md)
以了解相关要求。

贡献不一定需要写代码——不妨从改进文档开始？
标有 [good first issue](https://github.com/freqtrade/freqtrade/labels/good%20first%20issue) 的 issue 很适合作为首次贡献，也能帮助你熟悉代码库。

**注意**：在开始任何重大新功能的开发之前，*请先开一个 issue 描述你的计划*，或者在 [Discord](https://discord.gg/p7nuUNVfP7) 上与我们交流（请使用 #dev 频道）。这样感兴趣的人可以对该功能提供有价值的反馈，也能让其他人知道你正在做这件事。

**重要：** 请始终向 `develop` 分支提交 PR，而不是 `stable`。

## 系统要求

### 准确的时钟

时钟必须准确，并需频繁与 NTP 服务器同步，以避免与交易所通信时出现问题。

### 最低硬件要求

运行此机器人，我们建议使用至少满足以下配置的云服务器：

- 最低（建议）系统要求：2GB 内存、1GB 磁盘空间、2 个 vCPU

### 软件要求

- [Python >= 3.12](http://docs.python-guide.org/en/latest/starting/installation/)
- [pip](https://pip.pypa.io/en/stable/installing/)
- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [TA-Lib](https://ta-lib.github.io/ta-lib-python/)
- [virtualenv](https://virtualenv.pypa.io/en/stable/installation.html)（推荐）
- [Docker](https://www.docker.com/products/docker)（推荐）
