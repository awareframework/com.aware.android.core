Copyright (c) 2014 AWARE Mobile Context Instrumentation Middleware/Framework (http://www.awareframework.com)

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

# AWARE Android

**This repository is under development and not ready for use yet.**

This repository contains the the modules for each aware sensors. 

## Example usage

In your app `build.gradle` add the dependency to the module.

```gradle
dependencies {
    api project(':aware-accelerometer')

    // Other dependencies..
}
```

In your source code build the sensor.

```kotlin
val accelerometer = Accelerometer.Builder(appContext)
        .setDebug(true)
        .setDeviceId(UUID.randomUUID().toString())
        .setSensorObserver(object : SensorObserver {
            override fun onDataChanged(type: String, data: Any?, error: Any?) {
                // Your code here..
            }
        })
        .build()
accelerometer.start()
```