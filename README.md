<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Thawatchai-204/240-311">
    <img src="images/logo_readme.png" alt="Logo" width="150" height="150">
  </a>

  <h3 align="center">Book Shop Website</h3>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Component of Code</a>
      <ul>
        <li><a href="#prerequisites">public</a></li>
        <li><a href="#installation">routes</a></li>
      </ul>
    </li>
    <li><a href="#usage">Admin page</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

เป็นเว็บไซต์ในการกดสั่งซื้อหนังสือต่างๆ โดยมีระบบหลังบ้านในการบันทึกแก้ไขข้อมูลสินค้าต่างๆ
โดยเริ่มแรกให้ user login เข้าสู่ระบบสมาชิกในหน้าเว็บไซต์ เพื่อเข้าดูเลือกซื้อหนังสือภายในเว็บไซต์
โดยถ้าผู้ใช้จะทำการสั่งซื้อหนังสือก็ทำการกดปุ่มเพื่อสั่งซื้อหนังสือไปในตะกร้า

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![Node][Node.js]][Node-url]
* [![Ejs][Ejs]][Ejs-url]
* [![Express][Express.js]][Express-url]
* [![BOOTSTRAP][BOOTSTRAP]][BOOTSTRAP-url]
* [![MongoDB][MongoDB]][MongoDB-url]
* [![HTML][HTML]][HTML-url]
* [![JavaScript][JavaScript]][JavaScript-url]
* [![CSS][CSS]][CSS-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- Component of Code -->
## Component of Code

* models

product.js เป็นการเชือมไปยัง MongoDB  เพื่อใช้เก็บ Schema เก็บข้อมูลต่างๆคือ 
ข้อมูล name,price,image,description และส่งออกสำหรับบันทึกข้อมูล

### public
* CSS
ใช้สำหรับตกแต่งไฟล์ ejs ให้มีความสวยงามมากขึ้น
* image
เก็บไฟล์รูปภาพต่างๆ
* js
เก็บไฟล์ bootstrap jquery popper

### routes
* myRouter.js 
ใช้สำหรับการ route path ของไฟล์ในโฟล์เดอร์ views ไป link ตาม path ที่กำหนด
โดยมีการกำหนด path ไปยังหน้าต่างๆ ดังนี้


1. router '/' แสดงเป็นหน้าแรก คือ หน้า login
    ```
2. router '/index' แสดงเป็น product หนังสือเล่มต่างๆ ในหน้าเว็บไซต์
   ```
3. router '/login' ใช้สำหรับแสดงหน้า login สำหรับเข้าสู่หลังบ้านแอดมินเพื่อทำการลบเพิ่มแก้ไขข้อมูลหนังสือในเว็บไซต์ โดยมีการตรวจสอบ username และ password ว่าตรงเงื่อนไขที่กำหนดหรือไม่ ถ้าตรวจสอบแล้วตรงเงื่อนไข จะมีการสร้าง session โดยมีการกำหนด timeExpire เป็นเวลา 30 วินาที
โดยเมื่อ session มีการหมดอายุทางหนาเว็บก็จะ redirect เส้นทางใหม่ไปที่หน้า manage เพือต้องการ login เข้าสู้ระบบใหม่อีกครั้ง แล้วถ้าตรวจสอบแล้วรหัสมีการผิดพลาดจะแสดงผล 'ขออภัยเข้าสู่ระบบไม่สำเร็จ'
   ```
4. router '/logout' เป็นปุ่ม logout เพื่อออกจากระบบหลังบ้านหรือออกจากเว็บไซต์เพื่อเข้ามาสู่ระบบใหม่อีกครั้ง
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- Adnin page -->
## Amdin page

* router '/manage'
  router '/delete/:id'  เพื่อลบหนังสือออกจากฐานข้อมูลในเว็ปไซต์
  router '/edit'        เพื่อแก้ไขข้อมูล ชื่อสินค้า ราคา และ รายละเอียดหนังสือ
  router '/update'      เพื่อเป็นการอัพเดตข้อมูลหนังสือเข้าไปฐานข้อมูลของเว็บไซต์
  
* router '/add-product' 

  router '/insert'      เพื่อเป็นการบันทึกข้อมูลสิ้นค้ารูปภาพหนังสือและราคาเข้าไปในฐานข้อมูล
  โดยทั้ง 2 route ไม่มี session redirect ไป render เป็นหน้า admin เพื่อเข้าสู่หน้าเข้าระบบใหม่
 


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


รูปภาพนะจ๊ะ
<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png

[Node.js]: https://img.shields.io/badge/Node.js-V.1.0.0-339933?style=for-the-badge&logo=Node.js
[Node-url]: https://nodejs.org/en

[Ejs]: https://img.shields.io/badge/Ember.js-V.3.1.9-E04E39?style=for-the-badge&logo=Ember.js
[Ejs-url]: https://ejs.co/

[Express.js]: https://img.shields.io/badge/ExpressVPN-V.1.17.3-DA3940?style=for-the-badge&logo=ExpressVPN
[Express-url]: https://expressjs.com/

[BOOTSTRAP]: https://img.shields.io/badge/Bootstrap-V.5.3.0-7952B3?style=for-the-badge&logo=Bootstrap
[BOOTSTRAP-url]: https://angular.io/

[MongoDB]: https://img.shields.io/badge/MongoDB-V.6.0-47A248?style=for-the-badge&logo=MongoDB
[MongoDB-url]: https://www.mongodb.com/

[HTML]: https://img.shields.io/badge/HTML5-V.5-E34F26?style=for-the-badge&logo=HTML5
[HTML-url]: https://www.w3schools.com/html/

[JavaScript]: https://img.shields.io/badge/JavaScript-V.4.7-F7DF1E?style=for-the-badge&logo=JavaScript
[JavaScript-url]: https://www.javascript.com/

[CSS]: https://img.shields.io/badge/CSS3-V.3-1572B6?style=for-the-badge&logo=CSS3
[CSS-url]: https://www.w3schools.com/css/css_website_layout.asp
