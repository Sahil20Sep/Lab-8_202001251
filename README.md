# IT314: SOFTWARE ENGINEERING (Sec-B)
# LAB-8 (Group 28)
## _Name: Sahil Mangukiya_
## _Student ID: 202001251_
## _Objective: JUnit Testing in Eclipse_

### Writing Boa class in java.
```
public class Boa{
    private String name;
    // the length of the boa, in feet
    private int length; 
    private String favoriteFood;
    public Boa (String name, int length, String favoriteFood){
        this.name = name;
        this.length = length;
        this.favoriteFood = favoriteFood;
    }
    // returns true if this boa constructor is healthy
    public boolean isHealthy(){
        return this.favoriteFood.equals("granola bars");
    }
    // returns true if the length of this boa constrictor is
    // less than the given cage length
    public boolean fitsInCage(int cageLength){
        return this.length < cageLength;
    }
}
```
