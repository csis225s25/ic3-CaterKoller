# In Class Problem Set 3

I used ComboBoxDemo.java a few years ago.  It used to compile cleanly.  Even though the code has not changed, it now  will not compile without throwing warnings.

Doing everything from a command prompt or Git Bash (no IDEs allowed), your mission is to debug the code and find out why it stopped compiling cleanly.  When you have figured it out,  note what you changed and why it stopped working in the README.md file.


**Changes to code**
1. static JComboBox cBox1; -> static JComboBox<String> cBox1;
2. cBox1 = new JComboBox(s1); -> cBox1 = new JComboBox<String>(s1);

**What caused it to stop working?**
The problem was caused by unsafe operations due to not specifying a datatype for the object. Without the check for data that the object will store, it can cause errors in the code if the wrong type of data is passed into the constructor.
