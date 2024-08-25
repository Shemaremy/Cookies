# I just used cookies in this website


## Intro :

To manage cookies in your React component and handle accepting and rejecting cookie terms, you can use the browser's localStorage or cookies to store the user's preferences . Here's how you can manage it by storing a flag when the user accepts or rejects the terms, and ensuring the modal does not appear again if they have already made a choice.

- But I used local storage because it can store up to 5MB data
- While cookies store up to 4kb data




## What happened in my code (beginner version):

- useEffect checks whether the user has previously made a cookie consent decision when the page first loads.
- localStorage.getItem("cookieConsent") retrieves the value of cookieConsent from the browser's localStorage (which is a way to store data in the browser that persists between page reloads or visits). 

- If the user previously accepted or rejected cookies, this value will be either "accepted" or "rejected".
- If cookieConsent is null (meaning no consent has been stored yet), the modal is shown by setting modal to true using setModal(true).

- localStorage.setItem("cookieConsent", "accepted") saves the string "accepted" to localStorage with the key "cookieConsent". 

- This signifies that the user has accepted the cookies.
- setModal(false) hides the modal by setting modal to false, because the user has now made a choice.


