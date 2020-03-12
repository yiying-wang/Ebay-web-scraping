# Ebay web scraping-- Which sellers advertise/sponsor on eBay

### In this code, I will find out sponsor and nonsponsored items of Ipad 4 on ebay website. Then show the summary statistics of two groups and see the difference between them.

### steps are as follows:
#### a.
For the first 10 pages of 100 items/page, save all the URLs of sponsored items' pages to the file "sponsored.txt"  and all the URLs of non-sponsored items' pages to the file "non-sponsored.txt" in the same directory as your code. (One URL per line in each file)

#### b.
Create two folders in the same directory as your code and name them "sponsored" and "non-sponsored". Write a program that opens the two files and downloads each of the pages (URLs) into the folders "sponsored" and "non-sponsored". Each file should be named as "<item-id>.htm" where you replace "item-id" with the ID of the item you are saving.

#### c.
Write a separate piece of code that loops through the pages you downloaded in (c) and opens and parses them into a Python or Java xxxxsoup-object. Identify and select:

seller name, seller score, item price, # items sold, best offer available, title, returns allowed, shipping price, condition (e.g., used, new, like new, seller refurbished, ...).

#### d.
connect to SQL. Create a database and name it "eBay". Save the information of items into a single table named "eBay_items" (You are allowed to use only one table). This table should contain both sponsored and non-sponsored information and have a column that specifies which item is sponsored/non-sponsored.  If an item misses ANY of the information in (d), you should insert that missing value as NULL into the table. Convert any price (item price and shipping price) into a "dollar-cent" format (e.g., convert $12.34 into 1234 and $12 into 1200. Make sure the two least significant digits are cents. If an item does not include cents in the price, insert zeros.) and insert the price as INT into the table.

#### e.
run summary stats on each item. Print to the screen the mean, min, max, and mean for each column, grouped by "sponsor/non-sponsor" and "condition" (group by at the same time, not separately). For binary categorical columns, use 0-1 conversion. For e.g., for the "returns allowed" convert YES to 1 and NO to 0 and then calculate the stats.

## Difference on sponsored items and nonsponsored items:
1. all the sellers of the sponsored items have seller score, but the minimum of nonsponsor is normally zero
2. all the sponosored items have minimum item price
3. non-sponsored items have a higher return allow rate
4. sponsored items mostly have free shipping, non-sponsored items have higher shipping price

