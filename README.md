# TinyMDE with Undo and Redo support

Live Demo: <https://movsb.github.io/tinymde-with-undo-redo/>.

Issue: <https://github.com/jefago/tiny-markdown-editor/issues/44>.

> jefago: yeah, undo/redo events are definitely not handled deliberately, and I don't think it's easy to add proper undo/redo handling so I'm not really planning to add that.

Because of the lack of Undo/Redo support for TinyMDE and the author is not planned for implementing this feature currently and I'm eager for having this to work,
I tried to implement an inefficient one by using undo/redo stacks. It's inefficient because it saves the whole content every time it save a undo step. But, it looks good to me.
It works someway at least.

All source code is in the page, there's just only a new class UndoRedoStack. Construct it with the Editor, and then call the undo/redo method.
