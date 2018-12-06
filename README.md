import java.lang.reflect.Array;
import java.util.Arrays;
import java.util.Collection;

import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.Parameterized;
import org.junit.runners.Parameterized.Parameters;

// first step
@RunWith(Parameterized.class)
public class Parameter_testcase 
{
	
	//second step - defining parameters
	String firstname;
	String lastname;
	String password;
	int age;
	
	
	//third step
	public Parameter_testcase(String firstname, String lastname, String password, int age)
        {
		
		this.firstname = firstname;
		this.lastname = lastname;
		this.password = password;
		this.age = age;
		
		
	}
	

	//fourth step
	
	@Parameters
	public static Collection<Object[]> getData()
        {
		
		Object[][] data = new Object[2][4];
		
		//first row
		data[0][0]="Joy";
		data[0][1]="Smith";
		data[0][2]="Abcd";
		data[0][3]=18;
		
		//SECOND row
		data[1][0]="Tom";
		data[1][1]="Williams";
		data[1][2]="Abcde";
		data[1][3]=28;
		
		return Arrays.asList(data);
		
	}
	
	@Test
	public void doLogin()
        {
		
		System.out.println(firstname+" - "+lastname+" - "+password+" - "+age);
				
	}
	

}
