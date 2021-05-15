# recursionApproach

### Sort a stack
```java
    class sortAStack{
	public Stack<Integer> sort(Stack<Integer> s)
	{
		if(s.size()<=1)
		    return s;
		int temp = s.pop();
		s = sort(s);
		return insert(s,temp);
	}
	
	public Stack<Integer> insert(Stack<Integer> s, int val)
	{
	    if(s.size()==0 || s.peek()<=val)
	   {
	       s.push(val);
	       return s;
	   }
	   int temp = s.pop();
	   s = insert(s,val);
	   s.push(temp);
	   return s;
	}
}
```
