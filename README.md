# Option-price-parser
Option price parser from iss.moex

Structure of base url
'https://iss.moex.com/iss/engines/futures/markets/options/\
securities/{Ticker_base_asset[i]}{h}B{Month_OPT[j]}9/candles.csv?from=\
2019-01-01&till=2020-01-01&interval=24&iss.meta=on'

from = Дата, начиная с которой необходимо начать выводить данные.
Формат: ГГГГ-ММ-ДД.
till Дата, до которой выводить данные.
Формат: ГГГГ-ММ-ДД.
interval=24 - daily timeframe
Ticker_base_asset = list if base assets for option
Month_OPT = list of expiration months. For option call from A to L means from January to December. For put from M to X
Strikes = [step of strikes, min strike, max strike] order of strikes and base assets must be equal.
In url each strike takes place instead of {h}

For every ticker it is makes separate csv file

It works slow and it is normal.

Additional info:
https://iss.moex.com/iss/reference/
https://www.moex.com/a2193
