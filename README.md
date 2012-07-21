URLPatterns
====
URLs component-based input and output Patterns in the Python language.  
Matching URLs against Regular Expressions is straight forward, however outputting those URLs given a certain pattern is not.  
Pattern is a Python module to match URL strings against **INPUT PATTERNS** and output new URL strings based on **OUTPUT PATTERN**.  
This library was made for filtering adult content in private networks.
  
Syntax:
---
- New feature syntax: **<code>\<re:regex:end\></code>**, regex: can take any regular expression syntax.  



Examples:  
---

URL syntax:**<code> \<scheme name\> : \<hierarchical part\> [ ? \<query\> ] [ # \<fragment\> ]</code>**  
  
Input pattern:**<code> \<\*\>://youtube.com/\<\*\>/watch?\<\*\>v=\<\*\>#\<\*\></code>**  
Testing URL: **<code>http://www.youtube.com/watch?v=xyz</code>**  
Match Result: **<code>True</code>**  
Output pattern: **<code>\<s\>://youtube.com/\<q=v:name\>/\<q=v:value\></code>**  
Result URLs: **<code>http://youtube.com/v/xyz</code>**  
  
Input pattern: **<code>\<\*\>://twitter.com/\<\*\>#!/\<\*\></code>**  
Testing URL:  **<code>http://twitter.com/#!/xyz</code>**  
Match Result: **<code>True</code>**  
Output pattern: **<code>\<s\>://twitter.com/users/show_for_profile.json?screen_name=\<f:[2,]\></code>**  
Output pattern: **<code>\<s\>://twitter.com/users/\<f\></code>**  
Result URLs: **<code>http://twitter.com/users/show_for_profile.json?screen_name=xyz</code>**  
Result URLs: **<code>http://twitter.com/users/!/xyz</code>**  

