# windows os.system delete tmp

import os


def main():
    # <yes> <report> PYTHON_INJECTION_COMMAND shell1 <yes> <report> PYTHON_LOG_DEL pylogdelwinossysdelcwintemp
    os.system("del /S /Q C:\Windows\Temp\*")
    # <yes> <report> PYTHON_INJECTION_COMMAND shell1 <yes> <report> PYTHON_LOG_DEL pylogdelwinossysdeltemp
    os.system("del /S /Q %temp%\*")
    # <yes> <report> PYTHON_INJECTION_COMMAND shell1 <yes> <report> PYTHON_LOG_DEL pylogdelwinossysdeltmp
    os.system("del /S /Q %tmp%\*")


if __name__ == "__main__":
    main()

# windows shutil.rmtree delete tmp

import os
import shutil


def main():
    # <yes> <report> PYTHON_LOG_DEL pylogdelwinshutilcwintemp
    shutil.rmtree("C:\Windows\Temp", ignore_errors=False, onerror=None, dir_fd=None)
    # <yes> <report> PYTHON_LOG_DEL pylogdelwinshutiltmp
    shutil.rmtree("%tmp%", ignore_errors=False, onerror=None, dir_fd=None)
    # <yes> <report> PYTHON_LOG_DEL pylogdelwinshutiltemp
    shutil.rmtree("%temp%", ignore_errors=False, onerror=None, dir_fd=None)


if __name__ == "__main__":
    main()


# windows os.remove delete tmp

import os


def delTMPCWind() -> None:
    # <yes> <report> PYTHON_FILE_SEPARATOR_HARDCODED 9528cd
    files = os.listdir("C:\Windows\Temp")
    for file in files:
        if os.path.isdir(f"C:\Windows\Temp\\{file}"):
            pass
        else:
            # <yes> <report> PYTHON_LOG_DEL pylogdelwinosremcwintemp
            os.remove(f"C:\Windows\Temp\\{file}")


def delTMPTMP() -> None:
    files = os.listdir("%TMP%")
    for file in files:
        if os.path.isdir(f"%TMP%\\{file}"):
            pass
        else:
            # <yes> <report> PYTHON_LOG_DEL pylogdelwinosremtmp
            os.remove(f"%TMP%\\{file}")


def delTMPTEMP() -> None:
    files = os.listdir("%TEMP%")
    for file in files:
        if os.path.isdir(f"%TEMP%\\{file}"):
            pass
        else:
            # <yes> <report> PYTHON_LOG_DEL pylogdelwinosremtemp
            os.remove(f"%TEMP%\\{file}")


def main():
    delTMPCWind()
    delTMPTMP()
    delTMPTEMP()


if __name__ == "__main__":
    main()


# linux os.system delete tmp

import os


def main():
    # <yes> <report> PYTHON_INJECTION_COMMAND shell1 <yes> <report> PYTHON_LOG_DEL pylogdellinossystrmrf
    os.system("rm -rf /var/log/*")


if __name__ == "__main__":
    main()

# linux shutil.rmtree delete tmp

import os
import shutil


def main():
    # <yes> <report> PYTHON_LOG_DEL pylogdellinshutil
    shutil.rmtree("/var/log", ignore_errors=False, onerror=None, dir_fd=None)
    # <yes> <report> PYTHON_INJECTION_COMMAND shell1
    os.system("echo files were deleted")


if __name__ == "__main__":
    main()

#linux os.remove delete tmp

import os


def main():
    # <yes> <report> PYTHON_FILE_SEPARATOR_HARDCODED 9528cd
    files = os.listdir("/var/log")
    for file in files:
        if os.path.isdir(f"/var/log/{file}") or os.path.islink(f"/var/log/{file}"):
            pass
        else:
            # <yes> <report> PYTHON_LOG_DEL pylogdellinosrem
            os.remove(f"/var/log/{file}")


if __name__ == "__main__":
    main()
