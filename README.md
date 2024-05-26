Ристе Џајковски 222026

<b>CFG</b>

![Untitled Diagram (2)](https://github.com/Dzajko21/SI_2024_lab2_222026/assets/92513065/32e90b79-01aa-44af-9777-48eda10ea72c)
<hr>
Цикломатската комплексност на дадениот код изнесува 10.Ја добив според формулата V(G)=P+1,каде што P го означува бројот на предикатни јазли,а во кодот бројот на предикатни јазли е 9.
<hr>

<b>Every Branch</b>


Test Case 1: Null Item List<br>
•	Input: allItems = null, payment = 100<br>
•	Expected Output: RuntimeException with message "allItems list can't be null!"<br>
•	Description: Tests the branch where allItems is null.<br>


Test Case 2: Empty Item List<br>
•	Input: allItems = [], payment = 100<br>
•	Expected Output: true<br>
•	Description: Tests the branch where allItems is an empty list.<br>


Test Case 3: Item with Null Name<br>
•	Input: allItems = [new Item(null, "12345", 100, 0.1f)], payment = 100<br>
•	Expected Output: true<br>
•	Description: Tests the branch where item.getName() == null and the name should be set to “unknown”.<br>


Test Case 4: Item with Empty Name<br>
•	Input: allItems = [new Item("", "12345", 100, 0.1f)], payment = 100<br>
•	Expected Output: true<br>
•	Description: Tests the branch where item.getName().length() == 0 and the name should be set to “unknown”..<br>


Test Case 5: Item with Null Barcode<br>
•	Input: allItems = [new Item("item1", null, 100, 0.1f)], payment = 100<br>
•	Expected Output: RuntimeException with message "No barcode!"<br>
•	Description: Tests the branch where item.getBarcode() == null.<br>


Test Case 6: Item with Invalid Barcode Character<br>
•	Input: allItems = [new Item("item1", "123a5", 100, 0.1f)], payment = 100<br>
•	Expected Output: RuntimeException with message "Invalid character in item barcode!"<br>
•	Description: Tests the branch where allowed.indexOf(c) == -1.<br>


Test Case 7: Item with Valid Barcode and No Discount<br>
•	Input: allItems = [new Item("item1", "12345", 100, 0.0f)], payment = 100<br>
•	Expected Output: true<br>
•	Description: Tests the branch where item.getDiscount() == 0.<br>


Test Case 8: Item with Valid Barcode and Discount<br>
•	Input: allItems = [new Item("item1", "12345", 100, 0.1f)], payment = 10<br>
•	Expected Output: true<br>
•	Description: Tests the branch where item.getDiscount() > 0.<br>


Test Case 9: Special Discount Condition Met<br>
•	Input: allItems = [new Item("item1", "012345", 400, 0.1f)], payment = 100<br>
•	Expected Output: true<br>
•	Description: Tests the branch where item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0'.<br>


Test Case 10: Payment Less Than Sum<br>
•	Input: allItems = [new Item("item1", "12345", 100, 0.0f)], payment = 50<br>
•	Expected Output: false<br>
•	Description: Tests the branch where sum > payment.<br>

<hr>

<b>Multiple Condition</b>

Test Case 1: All Conditions True<br>
•	Input: allItems = [new Item("item1", "012345", 400, 0.1f)], payment = 100<br>
•	Expected Output: Sum adjusted by -30 if condition meets (validating later stages of flow) <br>
•	Description: Tests when all conditions are true. <br>


Test Case 2: Price True, Discount True, Barcode False<br>
•	Input: allItems = [new Item("item1", "112345", 400, 0.1f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when price and discount are true, but barcode condition is false. <br>


Test Case 3: Price True, Discount False, Barcode True<br>
•	Input: allItems = [new Item("item1", "012345", 400, 0.0f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when price and barcode conditions are true, but discount is false. <br>


Test Case 4: Price True, Discount False, Barcode False<br>
•	Input: allItems = [new Item("item1", "112345", 400, 0.0f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when only price condition is true. <br>


Test Case 5: Price False, Discount True, Barcode True<br>
•	Input: allItems = [new Item("item1", "012345", 200, 0.1f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when discount and barcode conditions are true, but price is false.<br>


Test Case 6: Price False, Discount True, Barcode False<br>
•	Input: allItems = [new Item("item1", "112345", 200, 0.1f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when only discount condition is true.<br>


Test Case 7: Price False, Discount False, Barcode True<br>
•	Input: allItems = [new Item("item1", "012345", 200, 0.0f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when only barcode condition is true.<br>


Test Case 8: All Conditions False<br>
•	Input: allItems = [new Item("item1", "112345", 200, 0.0f)], payment = 100<br>
•	Expected Output: Sum not adjusted by -30<br>
•	Description: Tests when all conditions are false.<br>

<hr>
