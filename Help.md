# Summary #

Memento Browser is a web browser that allows you "time-travel" through the Web by showing you web pages as they used to look in the past. These older versions are called "Mementos". The Mementos are archived web pages from the [Internet Archive](http://www.archive.org/), [WebCite](http://webcitation.org/), and other web archives.

# How It Works #

## Step 1: Click the Date Button ##

When you are viewing a web page as it exists today, you will see today's date in the **Displaying** field. To see an older version of the web page, click the **Date** button.

![http://cs.harding.edu/fmccown/memento/memento-browser-step1.png](http://cs.harding.edu/fmccown/memento/memento-browser-step1.png)

## Step 2: Select a Date ##

Select a month, day, and year from the past. The browser will attempt to find a page that was archived on that precise date, and it will load the page with the closet date that it could find. (You will likely not find any Mementos older than 1996.)

![http://cs.harding.edu/fmccown/memento/memento-browser-step2.png](http://cs.harding.edu/fmccown/memento/memento-browser-step2.png)

## Step 3: Viewing the Memento ##

After choosing a date, the Memento with the closest date is displayed. The URL will point to the archived page, and the date of the Memento will be displayed in the **Displaying** field.

![http://cs.harding.edu/fmccown/memento/memento-browser-step3.png](http://cs.harding.edu/fmccown/memento/memento-browser-step3.png)

You can use the **<** and **>** buttons to navigate to other archived versions of the web page. If you're finished time-traveling and want to return to how the web page looks today, click the **Now** button.

## Step 4: Viewing All Available Mementos ##

You may view all the Mementos available by clicking the **Choose Mementos** button from the action bar. The Mementos are grouped initially by year. When you select a date from the list of available Mementos, the selected Memento will appear in the browser.

![http://cs.harding.edu/fmccown/memento/memento-browser-step4.png](http://cs.harding.edu/fmccown/memento/memento-browser-step4.png)


# Date and Time Format #

You can change the date and time format by selecting **Settings** from the main menu and then selecting **Date & time settings**. Any changes to the settings will affect how the date and time are displayed in other applications.

# Timegates #

You may add your own custom timegates by selecting **Settings** from the main menu and selecting **Add timegate**. It is recommended you not add your own timegates unless you really know what you are doing. The default timegate at mementoproxy.lanl.gov cannot be deleted.

# FAQ #
## 1. What is a Memento? ##
_A Memento is an archived version of a web page at a particular date._

## 2. Where do these mementos come from? ##
_There are a number of web archives like [Internet Archive](http://archive.org/), [UK Web Archive](http://www.webarchive.org.uk/ukwa/), [WebCite](http://www.webcitation.org/), and others that supply mementos._

## 3. Why isn't there a Memento for every day? ##
_The Web is a very large place, and web archivists are not able to archive every web page every day._

## 4. Why can't I always push the Now button? ##
_If the web page you are viewing is the current version of the page, the Now button will be disabled._

## 5. Why are some web pages missing their pictures? ##
_When a web page is archived, especially older pages, its images aren't always archived._

## 6. Why does it take such a long time to find Mementos for some websites? ##
_Popular websites like cnn.com are archived frequently and therefore have more Mementos. Discovering the thousands of Mementos for these sites can take up to a minute or so._

# Technical Details #

Memento Browser is able to discover Mementos by sending Memento HTTP requests to a Timegate at mementoproxy.lanl.gov, a service created by the Prototyping Team at the Research Library of the Los Alamos National Laboratory. The Timegate aggregates archived pages from several web archives including the [Internet Archive](http://www.archive.org/), [WebCite](http://webcitation.org/), and others. The Internet Archive provides the majority of Mementos since they are the world's largest web archive. They began archiving the web in 1996, so you will not be able to find Mementos any older than what they have archived.

Memento is an addition to the HTTP protocol which allows a client to request an archived web resource from a specific date and time. Technical details about Memento can be found at the [Memento website](http://mementoweb.org/).

Memento Browser was built using the Android WebView object which allows limited control of the HTTP requests and responses it uses to load and render web pages. Therefore the browser is only able to support **simple mode** Memento. Simple mode is when the browser requests the web page's URL from a web archive, and it allows the web archive to return all the embedded images, style sheets, etc. This means that the archive is responsible for re-writing the embedded URLs so they reach back into the archive and not onto the "now" Web. This differs from **thorough mode** where the browser makes Memento requests for _all_ embedded resources.

# About #

Memento Browser was created by [Frank McCown](http://www.harding.edu/fmccown/) (Harding University). It is not as functional as major web browsers like Chrome and Firefox, but it gives you an idea of how these browsers could work in the future once Memento is widely adopted.

Memento Browser was created thanks to support from the Library of Congress and the National Science Foundation (Grant No. 1008492 - [WAC](http://www.harding.edu/fmccown/research/wac/)).