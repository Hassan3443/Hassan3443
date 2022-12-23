# Hassan Calculator app for Android

import android
import requests

def main():
  # Initialize the Android app
  app = android.Android()
  
  # Display the main menu
  app.dialogCreateAlert("Hassan Calculator")
  app.dialogSetItems(["Addition", "Subtraction", "Multiplication", "Division", "Currency Conversion"])
  app.dialogSetPositiveButtonText("Select")
  app.dialogShow()
  response = app.dialogGetResponse().result
  
  # Get the selected option
  option = response["item"]
  
  # Perform the selected operation
  if option == 0:
    # Addition
    app.dialogCreateInput("Addition", "Enter the first number:", "")
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    num1 = app.dialogGetResponse().result["value"]
    num1 = float(num1)
    
    app.dialogCreateInput("Addition", "Enter the second number:", "")
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    num2 = app.dialogGetResponse().result["value"]
    num2 = float(num2)
    
    result = num1 + num2
    app.dialogCreateAlert("Result", str(result))
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    
  elif option == 1:
    # Subtraction
    app.dialogCreateInput("Subtraction", "Enter the first number:", "")
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    num1 = app.dialogGetResponse().result["value"]
    num1 = float(num1)
    
    app.dialogCreateInput("Subtraction", "Enter the second number:", "")
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    num2 = app.dialogGetResponse().result["value"]
    num2 = float(num2)
    
    result = num1 - num2
    app.dialogCreateAlert("Result", str(result))
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    
  elif option == 2:
    # Multiplication
    app.dialogCreateInput("Multiplication", "Enter the first number:", "")
    app.dialogSetPositiveButtonText("Ok")
    app.dialogShow()
    num1 = app.dialogGetResponse().result["value"]
    num1 = float(num1)
    
    app.dialogCreateInput("Multiplication", "Enter the second number:", "")
    app
