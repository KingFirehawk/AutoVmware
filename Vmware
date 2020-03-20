import win32gui
import os
import time
import pyautogui


def get_window():
    hwnd_main = win32gui.FindWindowEx(None, None, None, "VMware Workstation")
    # print(hwnd_main)
    rect = win32gui.GetWindowRect(hwnd_main)
    get_window.x = rect[0]
    get_window.y = rect[1]
    get_window.w = rect[2]
    get_window.h = rect[3]
    # print("Window %s:" % win32gui.GetWindowText(hwnd_main))
    # print("\t   Top left: (%d, %d)" % (get_window.x, get_window.y))
    # print("\t   top right: (%d, %d)" % (get_window.w, get_window.y))
    # print("\t   Bottom left: (%d, %d)" % (get_window.x, get_window.h))
    # print("\t   Bottom right: (%d, %d)" % (get_window.w, get_window.h))


def click_opening(add):
    time.sleep(5)
    pyautogui.leftClick((get_window.x+101), (get_window.y+add))
    time.sleep(5)
    pyautogui.leftClick((get_window.x+324), (get_window.y+159))


def call_opening():

    os.startfile('C:\\Program Files (x86)\\VMware\\VMware Workstation\\vmware.exe')
    time.sleep(5)


instances = 5
add = 146
for x in range(instances):

    call_opening()  # 1
    get_window()  # calls def
    click_opening(add)  # calls def
    add += 18


# Helpful code

# pos = win32gui.GetCursorPos()
# print("\t   x,y (%d, %d)" % (pos))

# mouseX = pos[0]
# mouseY = pos[1]
