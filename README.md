# lab1_skirental

/* Javascript */
"use strict";
exports.__esModule = true;
var rl = require("readline-sync");
var item = rl.question("What are you buying/renting? ");
var cost_purchase = rl.question("How much does it cost to buy the ".concat(item, "? "));
var cost_rent = rl.question("How much does it cost to rent the ".concat(item, "? "));
var time_unit = rl.question("Renting costs $".concat(cost_rent, " per _____? (time unit) "));
var rent_time = rl.question("How many ".concat(time_unit, "s do you expect to rent? "));
var total_rent = cost_rent * rent_time;
var price_diff = total_rent - cost_purchase;
var rent_time_needed_to_equal_cost_of_purchase = cost_purchase / cost_rent;
console.log("Total expected rent cost: ".concat(total_rent));
if (price_diff >= 0) {
    console.log("It is cheaper to buy; you'd save $".concat(price_diff));
}
else {
    console.log("It is cheaper to rent; you'd save $".concat(-1 * price_diff));
}
console.log("The breakpoint even is ".concat(rent_time_needed_to_equal_cost_of_purchase, " ").concat(time_unit, "s"));


/* Typescript */
import * as rl from "readline-sync"

let item = rl.question("What are you buying/renting? ");
let cost_purchase : number = rl.question(`How much does it cost to buy the ${item}? `);
let cost_rent : number = rl.question(`How much does it cost to rent the ${item}? `);
let time_unit = rl.question(`Renting costs $${cost_rent} per _____? (time unit) `);
let rent_time : number = rl.question(`How many ${time_unit}s do you expect to rent? `);
let total_rent : number = cost_rent * rent_time
let price_diff = total_rent - cost_purchase
let rent_time_needed_to_equal_cost_of_purchase = cost_purchase / cost_rent
console.log(`Total expected rent cost: ${total_rent}`)

if (price_diff >= 0) {
    console.log(`It is cheaper to buy; you'd save $${price_diff}`)
}

else {
    console.log(`It is cheaper to rent; you'd save $${-1 * price_diff}`)
}

console.log(`The breakpoint even is ${rent_time_needed_to_equal_cost_of_purchase} ${time_unit}s`)
