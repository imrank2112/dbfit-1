## Store Query

`Store Query` reads out query results and stores them into a Fixture symbol for later use. Specify the full query as the first argument and the symbol name as the second argument (without `>>`). You can then use this stored result set as a parameter of the `Query` command later:

    !|Store Query|select n from ( select 1 as n union select 2 union select 3) x|firsttable|

    !|query|<<firsttable|
    |n                  |
    |1                  |
    |2                  |
    |3                  |

You can also directly compare two stored queries and check for differences.

