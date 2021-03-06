---
title: Murano Getting Started - Products - Python Simulator Script
template: default
---

# SIMULATE A DEVICE USING A PYTHON SCRIPT
**NOTE: This is a technical tutorial. You’ll need some familiarity with your operating system's terminal. In order to complete this tutorial you will need python installed on your system. If you haven’t used Python before, download and install it here: <a href="https://www.python.org" target="_blank">https://www.python.org/</a>**

In this tutorial, we'll simulate a device based on the "Connected Lightbulb Example" and see data on your dashboard.


# STEP 1: ADD EXAMPLE PRODUCT AND DEVICE

If you haven’t already, create a product using the connected lightbulb example here:
<a href="http://exosite.io/business/products" target="_blank">http://exosite.io/business/products</a>

![Add product button](assets/add_new_product.png )
![Create product for python device simulator](assets/create_product_python_simulator.png)

When you click on the "Definition" tab, it should look like this:
![Product Definition based on the example](assets/product_definition_lightbulb_example.png)

Now add a device with identity 000001, like so:
![Navigating to add new device](assets/product_add_device.png)
![Add new device modal](assets/new_device.png)
![Add new device modal](assets/product_device_not_activated.png)

It should show up in your list as not activated. Now we'll use the python device simulator to activate that device and start simulating data.


# STEP 2: RUN THE PYTHON DEVICE SIMULATOR

Open your OS terminal and clone the python simulator repo:
```
git clone https://github.com/exosite/murano_python_device_simulator_example.git
```

```
cd murano_python_device_simulator_example
```

Run the device simulator
```
python murano_device_simulator.py
```

The script will ask you for your ProductID. On your browser, navigate to your product on Exosite and copy your Product ID

![find product id](assets/find_product_id.png)

Paste it into terminal and hit enter

![terminal paste](assets/terminal_paste.png)

Then hit the enter key to use the default device identity (000001) - this matches the identity of the device you added earlier, so it will activate correctly.

**Note: If you've already added 000001 and simulated the device before, you may need to create a device (e.g. 000002), and change the default identity on the simulator. This will activate a new device and simulate data for it.**

If the Python Simulator is running correctly, it should look like this:
![Python simulator success](assets/product_python_simulator_success.png)

The script should show that the device has been activated and whether the lightbulb is on or off. Change back to your browser and make sure the device has been activated and data is showing up on the platform:
![Select device](assets/product_device_activated.png)

![Select device](assets/product_device_resources_simulated_data.png)

Awesome! Now you have a simulated device pumping data into Exosite. Keep the simulator running throughout these tutorials.


# STEP 3: CREATE THE DASHBOARD

On your browser, select the device you just created (most likely 000001) and open the Dashboard:
![Click Dashboard](assets/click_dashboard.png)

Add a text pane for temperature and include sparkline
 ![dashboard add pane](assets/product_dashboard_add_pane.png)
 ![dashboard add pane](assets/product_dashboard_add_widget.png)
 ![dashboard add widget](assets/dashboard_add_widget.png)

Do the same for Humidity. Then add a toggle switch for your light:
 ![dashboard add widget](assets/product_dashboard_toggle_widget.png)

Now try turning the light on and off for the simulated device. Hit the toggle switch on your dashboard, then switch to terminal (while the simulator is running) and make sure the simulator acknowledges it.
 ![dashboard toggle switch](assets/product_dashboard_complete_toggle_switch.png)
 ![dashboard toggle lightbulb on - terminal](assets/product_dashboard_lightbulb_on_terminal.png)

Congratulations - you just remotely turned a simulated device sensor on and off. 

<a class="btn orange" href="http://docs.exosite.com/murano/get-started/solutions/exampleapp/">UP NEXT: CREATE A SOLUTION >></a>
<div style="padding-bottom: 300px"></div>






