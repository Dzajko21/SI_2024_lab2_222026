Ристе Џајковски 222026

CFG

![Untitled Diagram (2)](https://github.com/Dzajko21/SI_2024_lab2_222026/assets/92513065/32e90b79-01aa-44af-9777-48eda10ea72c)

Цикломатската комплексност на дадениот код изнесува 10.Ја добив според формулата V(G)=P+1,каде што P го означува бројот на предикатни јазли,а во кодот бројот на предикатни јазли е 9.


Every Branch
Test Case 1: Null Item List
•	Input: allItems = null, payment = 100
•	Expected Output: RuntimeException with message "allItems list can't be null!"
•	Description: Tests the branch where allItems is null.
Test Case 2: Empty Item List
•	Input: allItems = [], payment = 100
•	Expected Output: true
•	Description: Tests the branch where allItems is an empty list.
Test Case 3: Item with Null Name
•	Input: allItems = [new Item(null, "12345", 100, 0.1f)], payment = 100
•	Expected Output: true
•	Description: Tests the branch where item.getName() == null and the name should be set to “unknown”.
Test Case 4: Item with Empty Name
•	Input: allItems = [new Item("", "12345", 100, 0.1f)], payment = 100
•	Expected Output: true
•	Description: Tests the branch where item.getName().length() == 0 and the name should be set to “unknown”..
Test Case 5: Item with Null Barcode
•	Input: allItems = [new Item("item1", null, 100, 0.1f)], payment = 100
•	Expected Output: RuntimeException with message "No barcode!"
•	Description: Tests the branch where item.getBarcode() == null.
Test Case 6: Item with Invalid Barcode Character
•	Input: allItems = [new Item("item1", "123a5", 100, 0.1f)], payment = 100
•	Expected Output: RuntimeException with message "Invalid character in item barcode!"
•	Description: Tests the branch where allowed.indexOf(c) == -1.
Test Case 7: Item with Valid Barcode and No Discount
•	Input: allItems = [new Item("item1", "12345", 100, 0.0f)], payment = 100
•	Expected Output: true
•	Description: Tests the branch where item.getDiscount() == 0.
Test Case 8: Item with Valid Barcode and Discount
•	Input: allItems = [new Item("item1", "12345", 100, 0.1f)], payment = 10
•	Expected Output: true
•	Description: Tests the branch where item.getDiscount() > 0.
Test Case 9: Special Discount Condition Met
•	Input: allItems = [new Item("item1", "012345", 400, 0.1f)], payment = 100
•	Expected Output: true
•	Description: Tests the branch where item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0'.
Test Case 10: Payment Less Than Sum
•	Input: allItems = [new Item("item1", "12345", 100, 0.0f)], payment = 50
•	Expected Output: false
•	Description: Tests the branch where sum > payment.

