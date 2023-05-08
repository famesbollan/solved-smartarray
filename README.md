Download Link: https://assignmentchef.com/product/solved-smartarray
<br>
<p class="ui header product-top-header" title="SmartArray Solution">Dynamically allocate space for a new SmartArray. Initialize its internal array to be of length length or DEFAULT_INIT_LEN, whichever is greater. (DEFAULT_INIT_LEN is defined in SmartArray.h.) Properly initialize pointers in the array to NULL, and set the size and capacity members of the struct to the appropriate values.

Output: “- Created new SmartArray of size &lt;N.” (Output should not include the quotes. Terminate the line with a newline character, ‘
’. &lt;N should of course be the length of the new array, without the angled brackets.)

Returns: A pointer to the new SmartArray, or NULL if any calls to malloc() failed. ree any dynamically allocated memory associated with the SmartArray struct and return NULL.

Returns: NULL pointer

Dynamically allocate a new array of length length. Copy the contents of smarty’s old array into the new array. Free any memory associated with the old smarty→array that is no longer in use, then set smarty→array to point to the newly created array. Be sure all pointers are properly initialized. Update the size and capacity of the SmartArray (ifapplicable).Note: If length is less than or equal to smarty’s current array capacity, or if the smarty pointer is NULL, you should NOT modify the SmartArray at all. In that case, just return from the function right away without producing any output.

Output: “- Expanded SmartArray to size &lt;N.” (Output should not include the quotes.Terminate the line with a newline character, ‘
’. &lt;N should be the new length of the array, without the angled brackets. Do NOT produce any output if you the array is not expanded.)

Returns: A pointer to the SmartArray, or NULL if any calls to malloc() failed.

If smarty’s capacity is greater than its current size, trim the length of the array to the current size. You will probably want to malloc() a new array to achieve this. If so, avoid memory leaks as you get rid of the old array. Update any members of smarty that need to be updated as a result of this action.

Output: “- Trimmed SmartArray to size &lt;N.” (Output should not include the quotes.Terminate the line with a newline character, ‘
’. &lt;N should be the new length of the array, without the angled brackets. Do NOT produce any output if the length of the array is not reduced by this function.)

Returns: A pointer to the SmartArray, or NULL if malloc() failed or if smarty was NULL.

Insert a copy of str into the next unused cell of the array. If the array is already full, call expandSmartArray() to grow the array to length (capacity * 2 + 1) before inserting the new element. When copying str into the array, only allocate the minimum amount of space necessary to store the string.

Returns: A pointer to the copy of the new string that was inserted into the array, or NULL if the string could not be added to the array (e.g., malloc() failed, or smarty or str was NULL).

Attempts to return the element at the specified index. This is where you protect the user from going out-of-bounds with the array.

Returns: A pointer to the string at position index of the array, or NULL if index was out of bounds or the smarty pointer was NULL.

If the array already has a valid string at position index, replace it with a copy of str. Otherwise, the operation fails and we simply return NULL. Ensure that no more space is used to store the new copy of str than is absolutely necessary (so, you might have to use malloc() and free() here).

Returns: A pointer to the copy of the string placed in the SmartArray, or NULL if the operation failed for any reason (e.g., invalid index, or smarty or str was NULL)

Insert a copy of str at the specified index in the array. Any elements to the right of index are shifted one space to the right. If the specified index is greater than the array’s size, the element being inserted should be placed in the first empty position in the array.As with the put() function, if the SmartArray is already full, call expandSmartArray() to grow the array to length (capacity * 2 + 1) before inserting the new element. When copying str into the array, only allocate the minimum amount of space necessary to store the string.

Returns: A pointer to the copy of the string inserted into the array, or NULL if insertion fails for any reason (e.g., malloc() failed, or smarty or str was NULL)

Remove the string at the specified index in the array. Strings to the right of index are shifted one space to the left, so as not to leave a gap in the array. The SmartArray’s size member should be updated accordingly. If index exceeds the SmartArray’s size, nothing is removed from the array.

Returns: 1 if an element was successfully removed from the array, 0 otherwise (including the case where the smarty pointer is NULL)

This function returns the number of elements currently in the array. We provide this function to discourage the programmer from accessing smarty→size directly. That way, if we decide to change the name or meaning of the size variable in our SmartArray struct, the programmers who download the latest version of our code can get it working right out of the box; they don’t have to go through their own code and change all instances of smarty→size to something else, as long as we provide them with a getSize() function that works.

Returns: Number of elements currently in the array, or -1 if the smarty pointer is NULL Print all strings currently in the array.

Output: Print all strings currently in the array. Print a newline character, ‘
’, after each string. If the SmartArray pointer is NULL, or if the array is empty, simply print “(empty array)” (without quotes), followed by a newline character, ‘
’

A double indicating how difficult you found this assignment on a scale of 1.0 (ridiculously easy) through 5.0 (insanely difficult)