---


---

<h1 id="text-editor-using-linked-list">Text Editor using Linked List</h1>
<h2 id="description">Description</h2>
<p>To make a text editor, a sequence of characters need to be stored. A cursor is used to help us locate where we want to be editing the sequence of text. This cursor will be between characters, and can be moved using the arrow keys. The cursor allows us to insert new characters at the cursor, and delete characters before the cursor. In a linked list based text editor, each character is considered as a node in the linked list and the insertion and deletion of characters follow the rules of linked list insertion and deletion.</p>
<p>The text editor is designed in C++ using QtCreator interface. QtCreator provides a GUI environment for the text editor. A QList (which is a container class of Qt and behaves as an arraylist) is used to store characters. An integer cursor variable is used. Characters are inserted into the list when a key is pressed. The functions like cut, copy and paste are implemented by inserting and removing characters from the list and the cursor variable is incremented or decremented.</p>
<h2 id="functions">Functions</h2>
<p><strong>void on_actionCut_triggered()</strong><br>
It is used to cut the selected portion of the text. If the start position of the selected text is after the cursor, the selected text is deleted from the start position but the cursor value is not changed. If the end position is before the cursor, the selected text is deleted from the start position and the cursor value is decremented by the length of the selected text.</p>
<p><strong>void on_actionCopy_triggered()</strong><br>
It is used to make a copy of the selected portion of the text. The selected text is appended to the list of characters.</p>
<p><strong>void on_actionPaste_triggered()</strong><br>
It is used to paste the selected text into the new location pointed to by the cursor. The function first checks whether a cut or copy command precedes the paste command. If true, then the text is added after the cursor and the cursor is incremented by size of selected text.</p>
<p><strong>void on_actionSave_triggered()</strong><br>
This function is used to save the file.</p>
<p><strong>void on_actionSave_As_triggered()</strong><br>
This function is used to save the file with a different name.</p>
<p><strong>void on_actionOpen_triggered()</strong><br>
This function is used to open the file for writing.</p>
<p><strong>void on_actionStatus_Bar_toggled(bool)</strong><br>
This function shows or hides the status bar.</p>
<p><strong>void keyPressEvent(QKeyEvent  <em>event)</em></strong><br>
This function is used to handle the exceptions that arise from pressing different keys such as backspace and Enter key.</p>
<p><strong>void keyReleaseEvent(QKeyEvent  <em>event)</em></strong><br>
This function is used to maintain the row number and column number of the text.</p>
<p><strong>Undo and Redo</strong><br>
For Undo and Redo operations, stacks are maintained of the cursor and the character list using C++ vector STL. At the end of each operation like entering a character, cut, copy and paste, the new cursor position and character list are pushed back into the stack and gives a snapshot of the operations and modifications done. When an undo operation is encountered, the variables are popped from the stack of operations and pushed into the redo stack. The redo stack stores the cursor position and list of characters after each undo operation. During a redo operation, the variables are popped from the redo stack and pushed into the stack of operations.</p>

