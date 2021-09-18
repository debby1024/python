'''
this will download and install a sample app (a calculator), 
add numbers to two input fields and show the sum of the two numbers
'''

from appium import webdriver
from appium.webdriver.common.mobileby import MobileBy
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time

desired_caps = {
    "deviceName": "iPhone 8",
    "platformName": "iOS",
    "version" : "12.1",
    "app": "https://testingbot.com/appium/sample.zip"
}

driver = webdriver.Remote("http://key:secret@hub.testingbot.com/wd/hub", desired_caps)

inputA = WebDriverWait(driver, 30).until(
    EC.element_to_be_clickable((MobileBy.ACCESSIBILITY_ID, "inputA"))
)
inputA.send_keys("10")

inputB = WebDriverWait(driver, 30).until(
    EC.element_to_be_clickable((MobileBy.ACCESSIBILITY_ID, "inputB"))
)
inputB.send_keys("5")

driver.quit()
