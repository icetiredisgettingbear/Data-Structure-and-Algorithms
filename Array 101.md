# [Array 101](https://leetcode.com/explore/featured/card/fun-with-arrays/521/introduction/)

배열을 아주 쉽고 적절하게 비유를 통해 설명하는 글을 발견했다. 안다고 생각하지 말고 기초부터 꼼꼼히 다시 공부하기! :fire: 

### What is an Array?
Array = storing DVDs in a box!  
> An Array is a collection of items. The items could be integers, strings, DVDs-anything really. The items are stored in neighboring contiguous memory locations, in definite size. Because they're stored together, checking through the entired collection of items is straightforward.

* a collection type
* only holds a sinlge type of data
* data is stored in contiguous memory location
* the definite size is decided on creation
* 0-indexed, meaning the highest index is arr.length-1

```java
public class arrayAndDVDs{
  DVD[] dvdCollection = new DVD[15];

  public class DVD{
    public String name;
    public int releaseYear;
    public String director;
    
    public DVD(String name, int releaseYear, String director){
      this.name = name;
      this.releaseYear = releaseYear;
      this.director = director;
  }
  
  public String toString(){
    System.out.println("Film : " + this.name + ", release Year : " + this.releaseYear + ", Director : " + this.director);
  }
}
```


### Default value for empty index
Java always initialises empty Array slot to **null** if it contains objects, or to default values if it contains primitive values.
  * int[] : 0
  * float[] : 0.0
  * bool[] : false

### Capacity vs Length
* Capacity : the maximum amount the array can hold e.g.) arr.length
* Length : the actual number of items that the array currently holds

> When an Array is given as a parameter, without any additional information, you can safely assume that **length == capacity**, therefore we can use arr.length.
