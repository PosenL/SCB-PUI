The program is use to roll out all applicable supply paths via the produced item to consumed item under the predefined plant.
For example:
If the target supply chain is from item A (consumed) to item F (produced) at plant TH70 to be rolled out via PUI table, the program will generate:
  1. **Input - JDA Source**: the input JDA table (where to target produced/counsumed item, the plant, and if the flow is multi-chip flow or not)
  2. **Initial - Rolling Supply Chain**: List down all paths if the consumed item can fully connects to the produced item. Will not be displayed if there is no connected structure between the produced and consumed item.
  3. **Analyzed - Rolling Supply Path**: Based on the result of 2., validate if there the plant is available in column K (JDA consumed plant = any available plant in the path), and further checking if there all plants in the combination are available in column L
                                     Column M consider the result of columns L and also check if the criteria of multi-chip is satisfied, then shows the final result if the combination is valid or not.
  4. **Result - PUI Mapping**: Based on the result of sheet 3., show the mapping result from PUI table if the SC has valid rolling structured.
  5. **Result - PUI Mapping (Drop_dup)**: Based on the result of sheet 4. and drop the duplicate records.
