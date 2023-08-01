# Project Title

Ecommerce-Store

---

## Project Description

---

This is a basic implementation of a throw out which will scrap primarily starting from the following url:

https://ecommerce-store-kohl-five.vercel.app/

It might take time upto ~= 15 to 20 minutes for the total scrapping to be completed depending on network speed. So, I request you to be patient after running the script and you can keep an eye on the console to have a rough idea about the progress of the process.

---

## Requirements

For development, you will only need Node.js and a node global package, NPM, installed in your environement.

External packages used:

    "lucide-react": "^0.263.1",
    "query-string": "^8.1.0",
    "clsx": "^2.0.0"

---

## Install

    $ git clone https://github.com/ZIAN786/ecommerce-store
    $ cd ecommerce-store
    $ npm install

## Running the project

    $ npm run dev

## Function Description:

<br/><br/>

> ### addItems (page) -->
>
> It fetches item urls + item ids (unique ids that the portal uses) from list page.

> ### individualItem (page) -->
>
> Shows how many category related for the provided initial url

> ### productItem (page) -->
>
> It shows the actual description and parses into the format: item id, title, price, size,color.

> ### getNextPageUrl (page) -->
>
> Previously mentioned other three functions are being invoked here.
> It primarily navigates to the next page. It will stop working if next page is not is available.

<br/><br/>

## Following are thoughts or questions/answers:

1. Used Try-Catch block wehre seemed necessary. Can use it in more places to making the error handling process smoother. We can use built-in timeout option in puppeteer to handle timeout errors.

2. I was not 100% sure about what was meant by "Accessing more ads from this link than the limit allows (max 50 pages)?". But I think we can replicate the API call format used by otomoto to access more data then we are allowed to access.

3. I have basic ideas about Github Actions as CI/CD tool. But can learn more jenkins or other similar tools if needed.

4. I've researched a bit and found that we can use mitm proxy tool for scrapping mobile applications (like otomot) but not 100% sure how to do that. But can give that a try later if needed.

5. The performance can be improved by adding some waiting function. (like waitForUntil and its various values).

6. We can expose this scrapper as an API using express.js along with other authentication/authorization systems and build a Front-End using ReactJS or VueJS and deploy it in a server and make it easily accessible for use.

7. Codes can be more cleaner by making it more modular. By modular I mean that extracting various functions to separate file and importing them from there to use in the main index.js file.
