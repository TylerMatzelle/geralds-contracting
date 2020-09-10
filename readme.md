# Gerald's Contracting

![Gerald]

This application will take the width and length of a house and return the number of studs required to frame the walls inside the 4x4 beams.
___
## How to use this application
To run a calculation, pass in two parameters:

* The width of one house (preceeded by the `-w` flag)
* The length of one house (preceeded by the `-l` flag)

Example: 
```
node dist/index.js -w 8 -l 8
```
___

### Scene
___

Gerald owns a construction company and builds single room homes. He can quickly create a rectangular house, usually within one day. He has found, however, that he spends a good amount of time calculating how much lumber he needs to buy for the walls.

Each corner of the house has a single 4x4 beam that walls can be nailed into and the trusses for the roof come pre-assembled. The only materials that Gerald needs to bring with him are the 2x4’s.

Gerald has decided to commission you to build him a simple application to calculate the number of 2x4’s he needs to buy so that he doesn’t have to make two trips to the store, but doesn’t buy too much. He’s given us the following information to help us calculate:
* Each wall has 2x4’s flat against the floor for the length of the edge of a wall.
* Each wall has vertical 2x4’s spaced 16 inches apart (measured from outside edge of a board to the next outside edge; the board is included in the 16 inches)
* Each wall has 2x4’s flat against the ceiling for the length of the edge of a wall.
* Gerald buys 10% MORE than a perfect calculation to account for waste
* Gerald notes that you can’t purchase a partial piece of lumber, so round up a decimal in the final calculation

* 2x4’s are actually 1.5" x 3.5”

* 4x4’s are actually 3.5” x 3.5”

* Gerald only buys 8’ 2x4’s

 Example
___

* Each wall is the same size in this case
* Each wall has two beams, totaling 7”, so the space in between is 7’ 5”.
* Each wall required one 2x4 on the top, bottom, and sides
* The remaining space across, broken into 16” sections, is 5.56, rounded up to 6.
* Total: 10 boards per wall, 40 boards for this house.

___
## Test log
| House Measurment | Studs Required | Application Returns | Last Test Run by |
| ---------------- | -------------- | ------------------- | ---------------- |
| 8x8              | 40             | 40                  | Tyler Matzelle   |
| 18x8             | 66             |                     | Tyler Matzelle   |
___

I used the [yargs package] for the processing of the command line parameters. For more information on that package go to the [yargs package] website.

[yargs package]: https://www.npmjs.com/package/yargs
[Gerald]: https://www.safetyandhealthmagazine.com/ext/resources/images/2016/04-april/construction-safety.jpg?t=1458739490&width=696# geralds-contracting
# geralds-contracting
