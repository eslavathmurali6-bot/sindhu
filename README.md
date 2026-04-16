from selenium import webdriver
from selenium.webdriver.common.by import By
import time

# Open Edge browser
driver = webdriver.Edge()

# Open Facebook
driver.get("https://www.instagram.com/")

# Wait for page to load
time.sleep(3)

# Enter Email
driver.find_element(By.ID, "email").send_keys("mani@gmail.com")

# Enter Password
driver.find_element(By.ID, "pass").send_keys("Murali@143")

# Click Login button
driver.find_element(By.NAME, "login").click()

# Wait for homepage to load
time.sleep(5)

# Check if login is successful
print("Current Page Title:", driver.title)

# Close browser
driver.quit()
