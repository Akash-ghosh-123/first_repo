---


---

<h1 id="welcome-to-stackedit">Welcome to StackEdit</h1>
<h2 id="text-editor-using-linked-list">Text Editor using Linked List</h2>
<p>To make a text editor, a sequence of characters need to be stored. A cursor is used to help us locate where we want to be editing the sequence of text. This cursor will be between characters, and can be moved using the arrow keys. The cursor allows us to insert new characters at the cursor, and delete characters before the cursor. In a linked list based text editor, each character is considered as a node in the linked list and the insertion and deletion of characters follow the rules of linked list insertion and deletion.</p>
<p><strong>void on_actionCut_triggered()</strong><br>
It is used to cut the selected portion of the text.</p>
<p><strong>void on_actionCopy_triggered()</strong><br>
It is used to make a copy of the selected portion of the text.</p>
<p><strong>void on_actionPaste_triggered()</strong><br>
It is used to paste the selected text into the new location pointed to by the cursor.</p>
<p><strong>void  on_actionSave_triggered()</strong><br>
This function is used to save the file.</p>
<p><strong>void  on_actionSave_As_triggered()</strong><br>
This function is used to save the file with a different name.</p>
<p><strong>void  on_actionOpen_triggered()</strong><br>
This function is used to open the file for writing.</p>
<p><strong>void  on_actionStatus_Bar_toggled(bool arg1)</strong><br>
This function shows or hides the status bar.</p>
<p><strong>void  keyPressEvent(QKeyEvent <em>event)</em></strong><br>
This function is used to handle the exceptions that arise from pressing different keys such as backspace and Enter key.</p>
<p>**void  keyReleaseEvent(QKeyEvent <em>event)<em>enter link description here</em></em><br>
This function is used to maintain the row number and column number of the text.</p>

