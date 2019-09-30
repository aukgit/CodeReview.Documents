# CodeReview.Documents
All code review guides will be share in here.

# Review Guide
- Value should be changed at once (only inside method can be changed 2 times in the wrost case if try catch is used.)
- Static Values should never be changed outside of the instance. (exception)
- Try to keep all the Static items to readonly. (exception : if changed inside class. There has to be a good reason for it.)
- All the magic `""` should be `constant` or `static readonly` (if project can be deployed part by part then use `static readonly` as must)
- Most of the created items should be readonly
- All the parameters should take Interfaces and output interface except for primitive type or JsonModel or DbModel.
- Every method should not have more than 3 arguments (worst), except for Utiliy or Helper static methods
    - Restrictions only one time use methods can have more arguments.
    - Solution wrap and create interface (parameter type interface)
- In a single method lines should NOT be more than 15 - 25 (worst)
- `Class` should **NOT** have more than 100-300 lines of code except for `Helper (Static)`
- Boolean datatype naming should starts with **`is`** (first choice) or `has`(if `is` doesn't go with naming then) or 'should' or 'does'
- Constants/static readonly collection or enum should be placed PersonalVpn.DataModel.StaticType Folder
- Each Item in the model folder/project should have `Model` as suffix.
- Copyable contents should be placed into `YourProjectNamespace.Content` Project
- Add a new line after the curly brace.
- All the `if`-`else`, `for`, `while`, `switch` should have braces. For javascript only use `if-else` avoid `switch`.
- Must follow C# *naming convention* and must use modifiers (access and others explicitly)
    - Follow Variable Naming Convention 
      - C#: http://bit.ly/305u3NX (only private instance objects will have underscore, no underscores)
      - Js: http://bit.ly/30m34xE (Don't use http://bit.ly/30d3NBn)
      - PowerShell: PascalCaseWith Hyphen (Get-Hello-World as function name.)
      - Css: http://bit.ly/30c6kM7 (Don't use http://bit.ly/30gaDWv)
      - Html: used class names should be in order.
- Only use spaces as indent. Must not use mixed of tabs and spaces. (IDE Settings : https://drive.google.com/open?id=1IWH0rUsQrOFf3dMFM2u6rC7xhHPd9cIh)
- Use string List for combinding string, don't use string builder. In place string modify create string builder for 100s of strings only. For 10-15 use simple contact.

```
string builder is used for smaller concatenation. StringBuilder is very useful or efficient when we do heavy string manipulation like 100s in one place . There is a downside to string-builder it also consumes more memory/performance if we think about smaller concatenation like 5-10. It is similar for Java and C#.   some articles : (C# - http://bit.ly/2YPc8dL, large manipulation stringbuilder is winner (http://bit.ly/2YTTmSq), another C#: http://bit.ly/2YQZ1sm)

String vs. StringBuilder
https://stackoverflow.com/questions/73883/string-vs-stringbuilder
```

- Used proper branch name (feature/YourGitHubTaskNumber-Title-with-hyphen)

# Tools Use for this Project
- Visual Studio 2017 Enterprise.
- TortoiseGit
- Github Desktop
- GitExtensions
- GitBash
- InnoSetup
- Beyond Compare
- OpenVpn
- Resharper (Plugin : Clean Code, Enhance ToolTip Plugin)

# IDE Settings
- https://drive.google.com/open?id=1IWH0rUsQrOFf3dMFM2u6rC7xhHPd9cIh
