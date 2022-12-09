Release 1.0.1
=============
* Bug fixes: startup fail when virtual driver mounted in system.
    `QMessageBox::critical(MainWindow::getInstance(), ...)` crash
    when try to obtain disk info in the startup process.
    the main window not ready, this `getInstance()` will create new instance again.
    so there will be a `getInstance()` loop...... program FATAL.
    I change this `QMessageBox::critical` to NULL parent.
* Update: using static-linked Qt5.9.6 with mingw and QtCreator9.0.0
* Changes: layout.


