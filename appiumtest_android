import os
import unittest
from appium import webdriver


class ContactAppTestAppium(unittest.TestCase):

    def setUp(self):
        desired_caps = {}
        desired_caps['platformName'] = 'Android'
        desired_caps['platformVersion'] = '4.4'
        desired_caps['deviceName'] = 'test1'
        desired_caps['app'] = 'https://testingbot.com/appium/sample.apk'
        desired_caps['appPackage'] = 'com.example.getstatus'
        desired_caps['appActivity'] = '.MainActivity'

        self.driver = webdriver.Remote('http://127.0.0.1:4723/wd/hub', desired_caps)

    def test_ClickRefreshLink(self):
        refreshButton  = self.driver.find_element_by_id("com.example.getstatus:id/fab")
        self.assertTrue(refreshButton.is_displayed())
        refreshButton.click()
        ## Right now we are just verify the displayed message on the Phone
        ## You can right code to handle that toast message and Verify that message


    def tearDown(self):
        self.driver.quit()

if __name__ == '__main__':
    suite = unittest.TestLoader().loadTestsFromTestCase(ContactAppTestAppium)
    unittest.TextTestRunner(verbosity=2).run(suite)

