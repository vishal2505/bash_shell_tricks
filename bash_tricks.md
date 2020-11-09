### How to extract one column of a csv file

We can use awk for this. Change '$2' to the nth column.

``` awk -F "\"*,\"*" '{print $2}' textfile.csv ```

### Print lines where a specific column has a length condition

``` awk -F"," 'length($2) != 10 { print }' /path/to/input > bad_field_length.txt ```
