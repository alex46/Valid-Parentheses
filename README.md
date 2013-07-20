Valid-Parentheses
=================


public class Solution {
public boolean isValid(String s) {
// Start typing your Java solution below
// DO NOT write main() function
Stack<Character> stack = new Stack();
for(int i = 0; i < s.length(); i++) {
char ch = s.charAt(i);
if(ch == '(' || ch == '{' || ch == '[') {
stack.push(ch);
}
if(ch == ')') {
if(stack.isEmpty() || stack.pop() != '(') return false;
//stack.pop();
}
if(ch == '}') {
if(stack.isEmpty() || stack.pop() != '{') return false;
//stack.pop();
}
if(ch == ']') {
if(stack.isEmpty() || stack.pop() != '[') return false;
//stack.pop();
}
}
return stack.isEmpty();
}
}
