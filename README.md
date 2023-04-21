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

![image](https://user-images.githubusercontent.com/118440195/233592060-1d4b3170-3461-4d46-ba9d-a65d8929c26c.png)


### Writing BoaTest in java.
```
import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	Boa jen, en;
	@Test
	public void testIsHealthy() {
		assertEquals("Error in isHealthy()", false, jen.isHealthy());
		assertEquals("Error in isHealthy()", true, jen.isHealthy());
		assertEquals("Error in isHealthy()", false, en.isHealthy());
		assertEquals("Error in isHealthy()", true, en.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		assertEquals("Error in fitsInCage()", true, en.fitsInCage(10));
		assertEquals("Error in fitsInCage()", true, en.fitsInCage(0));
		assertEquals("Error in fitsInCage()", false, en.fitsInCage(1));
		assertEquals("Error in fitsInCage()", false, en.fitsInCage(20));
	}
	
	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		en = new Boa ("Kenneth", 3, "granola bars");
	}
}
```
![image](https://user-images.githubusercontent.com/118440195/233595568-84c21773-d275-4812-80e8-b5daa46a8ab5.png)

![image](https://user-images.githubusercontent.com/118440195/233594653-13991162-e682-4860-aad2-f9d339d9d6f1.png)


### Now adding new Function.
```
public class Boa {
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
	// produces the length of the Boa in inches
	public int lengthInInches(int a){
	// you need to write the body of this method
		return (int) (a/2.5);
	}
}
```

```
import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	Boa jen,en;
	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		en = new Boa ("Kenneth", 3, "granola bars");
	}
	
	@Test
	public void testIsHealthy() {
		assertEquals("Error in isHealthy()",false,jen.isHealthy());
		assertEquals("Error in isHealthy()",true,jen.isHealthy());
		assertEquals("Error in isHealthy()",false,en.isHealthy());
		assertEquals("Error in isHealthy()",true,en.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		assertEquals("Error in fitsInCage()",true,en.fitsInCage(10));
		assertEquals("Error in fitsInCage()",1,en.fitsInCage(0));
		assertEquals("Error in fitsInCage()",false,en.fitsInCage(1));
		assertEquals("Error in fitsInCage()",0,en.fitsInCage(20));
	}
	@Test
	public void testLength() {
		assertEquals("Error in lengthInInches()",4,en.lengthInInches(10));
		assertEquals("Error in lengthInInches()",0,en.lengthInInches(0));
		assertEquals("Error in lengthInInches()",0,en.lengthInInches(1));
		assertEquals("Error in lengthInInches()",8,en.lengthInInches(20));
	}
}
```

![image](https://user-images.githubusercontent.com/118440195/233595104-c104d935-3b6b-48ca-b63e-1fdc45737915.png)

![image](https://user-images.githubusercontent.com/118440195/233595338-bb8551fe-aebf-4fcd-8820-066647728e8f.png)



















