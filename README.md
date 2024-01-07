import time
from appium import webdriver
from appium.webdriver.common.mobileby import MobileBy
from appium.webdriver.common.touch_action import TouchAction
import appium.webdriver.extensions.android.nativekey as nativeKey

from helpers.web_element_wrapper import *
desired_caps = {}
desired_caps["platformName"] = "Android"
desired_caps["automationName"] = "uiautomator2"
desired_caps["newCommandTimeout"] = 1000
desired_caps["app"] = "C:\\Users\\INFIQUITY TECH\\PycharmProjects\\Appiumtesting\\appium testing\\AppFiles\\v2.15.08.04.apk"
driver = webdriver.Remote('http://localhost:4723/wd/hub', desired_caps)
time.sleep(5)

device_window_size=driver.get_window_size()
start_x_cor = device_window_size['width']*3/4
y_cor=device_window_size['height']/2
end_x_cor=device_window_size['width']/15
actions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
acactions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
tions=TouchAction(driver)
actions.press(None,start_x_cor,y_cor,2.0).move_to(None,end_x_cor,y_cor).release().perform()
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/tvNext")').click()
# driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Skip")').click()
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Finish")').click()
create_profile=driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/SaveButton")')
assert create_profile.text=="CREATE PROFILE"
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Rider\'s Name")').is_displayed()==True
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/etUserName")').send_keys("CHAITRA")
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Location")').is_displayed()==True

driver.press_keycode(nativeKey.AndroidKey.DIGIT_0)
driver.press_keycode(nativeKey.AndroidKey.DIGIT_3)
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/etUserName")').text == "CHAITRA"

assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/etLocation")').send_keys("Bengaluru")
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR, value='resourceId("suzuki.com.suzuki:id/currentLocIv")').click()
#application_element=driver.find_element(by=MobileBy.CLASS_NAME,value="android.widget.TextView")
#assert application_element.is_displayed()==True

if(is_element_present(driver, MobileBy.ANDROID_UIAUTOMATOR, 'resourceId("suzuki.com.suzuki:id/tvAlertText")') == True):
    driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR, value='resourceId("suzuki.com.suzuki:id/ivCheck")').click()
    driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR, value='text("WHILE USING THE APP")').click()

# assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR, value='resourceId("com.android.permissioncontroller:id/permission_message")').is_displayed()==True
# # assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR, value='text("WHILE USING THE APP")').is_displayed()==True


 #Need to select again

# driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR, value='resourceId("suzuki.com.suzuki:id/currentLocIv")').click()

assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Your Ride")').is_displayed()==True
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Choose Your Ride Type")').is_displayed()==True
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Choose Your Ride Type")').click()
# # driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Scooter")').click()
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Motorcycle")').click()
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Choose Your Ride Model")').is_displayed()==True
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Choose Your Ride Model")').click()
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("GIXXER / GIXXER SF")').click()
# # target_name = "Pearl Blaze Orange"
# # motorcycle_images = driver.find_elements(by=MobileBy.ANDROID_UIAUTOMATOR, value='text("{}")'.format(target_name))
# # if len(motorcycle_images) >= 5:
# #  fifth_image = motorcycle_images[4]
# #  fifth_image.click()
#
# # assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("Access 125")').is_displayed()==True
# # driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("GIXXER / GIXXER SF")').click()
bike_section=driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/viewPager")')
device_window_size = driver.get_window_size()
start_x_cor = device_window_size['width'] * 3/4
y_cor = bike_section.location['y'] + 50
end_x_cor = device_window_size['width']/15
actions=TouchAction(driver)
actions.press(None,start_x_cor, y_cor, 2.0).move_to(None, end_x_cor ,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor, y_cor, 2.0).move_to(None, end_x_cor ,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor, y_cor, 2.0).move_to(None, end_x_cor ,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,start_x_cor, y_cor, 2.0).move_to(None, end_x_cor ,y_cor).release().perform()
actions=TouchAction(driver)
actions.press(None,end_x_cor, y_cor, 2.0).move_to(None, start_x_cor ,y_cor).release().perform()
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/slide")').is_displayed()==True
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/signup_tv")').is_displayed()==True
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/privacyCheckBox")').is_displayed()==True
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/privacyCheckBox")').click()
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/tvTermsConditions")').is_displayed()==True
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/SaveButton")').click()
# assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("com.miui.powerkeeper:id/action_bar_title_expand")').is_displayed()==True
# assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("BACKGROUND SETTINGS")').is_displayed()==True
# driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("android:id/checkbox")')
# assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='text("No restrictions")').click()
# assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("android:id/summary")').click()
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/tvAlertText")').is_displayed()==True
assert driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/ivCheck")').is_displayed()==True
driver.find_element(by=MobileBy.ANDROID_UIAUTOMATOR,value='resourceId("suzuki.com.suzuki:id/ivCheck")').click()
driver.quit()
