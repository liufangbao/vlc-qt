# How to contribute to VLC-Qt

## Feature Requests

It is a high possibility that we did not include all libVLC features into
the library. Feel free to open an issue describing your needed functionality.
Widgets and QML related ideas are also accepted.

If you can, you are encouraged to write the new features by yourself and submit
a pull request (more details below).

Please do not send send feature requests and bug reports via e-mail!


## Submitting Issues

Found a bug in VLC-Qt? Here are some guidelines on how to report the issue so
it can be resolved it as fast as possible:

- Explain in detail how to reproduce the issue.
- Include sample code you used, build output and other **relevant** information.
- Please include information on what VLC, Qt, VLC-Qt version you are using
  and what operating system you are running.


## Writing guides

I will prepare a special space on the web page for guides. More information soon.


## Pull Requests

To ease the pull request merge into mainline, please follow these requirements:

- The pull request title and message should be meaningful enough that reading
  the code is not necessary.
- Use similar coding style as you see in existing code, notably:
  
  - use 4 spaces indentation not tabs
  - private variables have underscore as a prefix ```_vlcInstance```
  - all public functions should be documented, for better readability put each
    argument in a new line
    ```c++
    /*!
        \brief Sets the application name.

        libvlc passes this as the user agent string when a protocol requires it.

        \param application Application name (QString)
        \param version Application version (QString)
    */
    void setUserAgent(const QString &application,
                      const QString &version);
    ```

- **One pull request per feature**. If you want to do more than one thing, send
  multiple pull requests. You should create a separate branch for each one.
- Make sure each individual commit in your pull request is meaningful.
  If you had to make multiple intermediate commits while developing, please
  squash them before sending them to us.
- Use git's [interactive rebase](https://help.github.com/articles/interactive-rebase)
feature to tidy up your commits before submitting the pull request.
- Your PRs must pass build tests on Travis and AppVeyor. We can assist you
  with support for other platforms that you work on, so please note where you
  tested the code before submitting the PR.