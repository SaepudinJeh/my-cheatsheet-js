# my-cheatsheet-js
Contains a collection of previously worked on function javascript cheat sheets

---

> Example filter and delete field
```javascript
const data = [
    {
        isBan: false,
        idAccount: "643baa6b2ec2982520e8585d",
        idUser: "643baa6b2ec2982520e8585f",
        _id: "643baa6b2ec2982520e8585d",
        countryId: "+62",
        email: null,
        fullName: "Brett Nicolas",
        phoneNumber: "85722440592",
        profiles: [],
        activeProfile: "643baa6b2ec2982520e8585c",
        social: [
            {
                _id: "6454fc728529d2fb77e663c1",
                provider: "google",
                email: "ilyas.syafii@gmail.com"
            },
            {
                _id: "644f553068a9c3413a18672b",
                provider: "facebook",
                email: "madara58senju@yahoo.com"
            }
        ],
        user: "643baa6b2ec2982520e8585f",
        createdAt: "2023-04-16T07:57:31.184Z",
        updatedAt: "2023-04-16T07:57:31.184Z"
    }
]

const newData = data.map(({ social, ...rest }) => ({
  ...rest,
  facebook: social.find(({ provider }) => provider === 'facebook'),
  google: social.find(({ provider }) => provider === 'google'),
}));
```
