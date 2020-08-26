# 1309.-Decrypt-String-from-Alphabet-to-Integer-Mapping

```C#
     public string FreqAlphabets(string s) {
     
        char[] chars = s.ToCharArray();
            string currentChar = "";
            var sol = new StringBuilder();

            for(int i=s.Length -1; i>=0; i--)
            {
                if(chars[i] == '#')
                {
                    currentChar = "" + chars[i - 2] + chars[i - 1];
                    i -= 2;
                }
                else
                {
                    currentChar = "" + chars[i];
                }

                char c = (char)(Int32.Parse(currentChar) + 96);
                sol.Append(c);

            }
        string stu = sol.ToString();
            return new string(stu.Reverse().ToArray());

     }
```

## Complexity Analysis
 
