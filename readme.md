## How to use SuperPY

Hello! Welcome and thank you for using SuperPY, the state of the art command line interface (CLI) for
Supermarket inventory management. The CLI is surprisingly easy to use!

IMPORTANT!!
Before first usage run this command: python main.py init

Remember: Prepend each command with: python main.py

You can run the following commands:

    - 'reinit' : Clear the stock and sold files, reset the id counters.

    - 'buy' : Buy a product and add it to your stock. 
        Required parameters: --productname : The name of the product you are buying.
                             --buyprice : The price you bought the product for.
                             --expirationdate : The products expiration date, in YYYY-MM-DD format
        For example:
            'python main.py buy --productname Herbs --buyprice 2.5 --expirationdate 2022-05-22'

    - 'stock' : Show a list of products currently in stock.

    - 'sales' : Show a list of products sold.

    - 'advancetime' : Advance time by the given amount of days, default is 1 day.
        Optional parameters: --days : The amount of days you want to progress by.
        For example: 
            'python main.py advancetime --days 3'

    - 'sell' : Sell a product.
        Required parameters: --productname : The name of the product you are selling.
                             --price : The price you are selling the product at.
        The CLI will check for you if the product is in stock and if it is not past it's expiration date.
        For example:
            'python main.py sell --productname Herbs --price 6'
    
    - 'revenue' : Return the revenue of a day, default is today.
        Optional parameters: --day: Which day's revenue you want in YYYY-MM-DD format.
        For example:
            'python main.py revenue --day 2021-04-13'

    - 'profit' : Return the profit of a day, default is today.
        Optional parameters: --day: Which day's profit you want in YYYY-MM-DD format.
        For example:
            'python main.py profit --day 2021-04-13'

    - 'clearstock' : Clear all expired items from your stock.

    - 'testdata' : Fills your stock with some items, sells some and advances time.

    - 'importjson' : The old system used json files. Use this to import the old registration system's data.
        Required parameters: --path, Relative path to the json file.
        For example:
            'python main.py importjson --path data/old_stock.json'

    - 'exportjson' : For compatibility issues the data can be exported as a Json file.
        Required parameters: --type, export sales or stock data.
        For example:
            'python main.py exportjson --type sales'

    - showgraph' : The newest feature of SuperPy! You can show your stock and sales in a bar chart format.
        Required parameters: --type, show sales or stock data.
        For example:
            'python main.py showgraph --type sales'

We hope you enjoy using our product!