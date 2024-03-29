# Useful Methods 

### Math
* Math.max(int a, int b) : return the maximum value between the two operands.

### Arrays
* Arrays.toString(array) : stringify the elements of an array
* Arrays.copyOf(array, newLength) : copying an array into another

### List Interface
* int size() : Returns the number of elements in the list.
* boolean isEmpty() : Returns true if the list is empty and false otherwise.
* boolean contains(Object o) : Returns true if there's the element in the list and false otherwise.
* get(int index) : Returns the element at the position
* set(int index, element) : Replaces the element at the specified position with the element taken.
* boolean add(element) : Appends the specified element to the end of the list and returns true.
* add(int index, element) : Inserts the specified element at the specified position and shifts the element currently at the position and any subsequent elements to the right
* boolean remove(Object o) : Removes the element with the lowest index and returns true if the list contained the specified element.
* remove(int index) : Removes the element at the specified position and shifts any subsequent elements to the left. Returns the removed element.
* int indexOf(Object o) : Returns the lowest index of the specified element, or -1 is this list doens't contain the element.
* boolean addAll(Collection c) : Copies all the elements of the collection and appends them at the end of the list. Returns true if the list's been changed.
  * ArrayList, LinkedList의 경우 생성자의 파라미터로 다른 컬렉션을 복사할 수도 있다.  
  `List<String> newArrayList = new ArrayList<String>(originalArrayList);`
* boolean addAll(int index, Collection c) : Do the same as above but at the specified position.
* boolean removeAll(Collection c) : Removes all the elements from the list that are contained in the specified collection. Returns true if the list's been changed.
* boolean retainAll(Collection c) : Retains only the elements that are in the specified collection and returns true if the list's been changed.


### String
* int compareTo(String s) : compares two strings lexicographically. In specific, compares the strings' unicode value. 
  * Unicode value : Upper cases have lower value than lower cases and the value increases in alphabetical order. 
  * returns 0, if the string is equal to the other string
  * returns negative difference, if the value of this string is smaller than the argument string's.
  * returns positive difference, if the value of this string is bigger than the arguemnt string's.
* char[] toCharArray() : converts this string to a new character array.
* char charAt(int index) : returns the char value at the specific index.
* String[] split(String regex) : splits this string around matches of the given regex.  
* boolean contains(String s) : returns true if this string contains the specified string.

<br/><br/>

+) Definition of lexicographical ordering by Java
> This is the definition of lexicographic ordering. If two strings are different, then either they have different characters at some index that is a valid index for both strings, or their lengths are different, or both. If they have different characters at one or more index positions, let <i>k</i> be the smallest such index; then the string whose character at position <i>k</i> has the smaller value, as determined by using the &lt; operator, lexicographically precedes the other string. In this case, {@code compareTo} returns the difference of the two character values at position {@code k} in the two string -- that is, the value: <blockquote><pre> this.charAt(k)-anotherString.charAt(k)</pre></blockquote> If there is no index position at which they differ, then the shorter string lexicographically precedes the longer string. In this case, {@code compareTo} returns the difference of the lengths of the strings -- that is, the value: <blockquote><pre> this.length()-anotherString.length()</pre></blockquote>
