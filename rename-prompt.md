You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "Blog.html",
    "context": {
      "title": "AUTHORISED AMAZON SERVICE PROVIDER IN JAIPUR",
      "first_heading": "What to do when you receive a damaged product from buyer in case of easy ship on Amazon?"
    }
  },
  {
    "path": "Privacy-Policy.html",
    "context": {
      "title": "AUTHORISED AMAZON SERVICE PROVIDER",
      "first_heading": ""
    }
  },
  {
    "path": "Product-Pricing-Display.html",
    "context": {
      "title": "AUTHORISED AMAZON SERVICE PROVIDER",
      "first_heading": ""
    }
  },
  {
    "path": "Refund-Cancelation-Policy.html",
    "context": {
      "title": "AUTHORISED AMAZON SERVICE PROVIDER",
      "first_heading": ""
    }
  },
  {
    "path": "Testimonials.html",
    "context": {
      "title": "AUTHORISED AMAZON SERVICE PROVIDER NETWORK , ONLINE BUSINESS CONSULTANTS & ADVISER",
      "first_heading": ""
    }
  },
  {
    "path": "blog_-find-out-why-great-india-sale-for-diwali-2017-is-the-golden-opportunity-for-all-the-sellers--.html",
    "context": {
      "title": "Find out Why Great India sale for Diwali 2017 is the Golden Opportunity for all the Sellers ?",
      "first_heading": "Find out Why Great India sale for Diwali 2017 is the Golden Opportunity for all the Sellers ?"
    }
  },
  {
    "path": "blog_4-easy-step-by-step-guide-on-how-to-get-started-with-amazon-for-beginners--what-are-the-required--documents-which-are-needed-to-start-selling-on-amazon-.html",
    "context": {
      "title": "4 easy step by step guide on How to get started with Amazon for beginners? What are the required documents which are needed to start selling on Amazon?",
      "first_heading": "4 easy step by step guide on How to get started with Amazon for beginners? What are the required documents which are needed to start selling on Amazon?"
    }
  },
  {
    "path": "blog_5-reason-why-you-should-start-selling-on-amazon-today-.html",
    "context": {
      "title": "5 Reason Why you Should Start Selling on Amazon Today?",
      "first_heading": "5 Reason Why you Should Start Selling on Amazon Today?"
    }
  },
  {
    "path": "blog_5-tips-on-how-to-increase-sales-on-amazon.html",
    "context": {
      "title": "5 Tips on How to increase sales on Amazon",
      "first_heading": "5 Tips on How to increase sales on Amazon"
    }
  },
  {
    "path": "blog_are-you-still-wondering-why-amazon-suspends--your-seller-accounts-.html",
    "context": {
      "title": "Are you still wondering Why Amazon Suspends your seller accounts?",
      "first_heading": "Are you still wondering Why Amazon Suspends your seller accounts?"
    }
  },
  {
    "path": "blog_how-to-do-apparel-photography-for-selling-on-amazon-.html",
    "context": {
      "title": "How to do Apparel Photography for selling on Amazon?",
      "first_heading": "How to do Apparel Photography for selling on Amazon?"
    }
  },
  {
    "path": "blog_how-to-increase-page-views-on-your-online-shop-in-marketplace-.html",
    "context": {
      "title": "How to increase Page Views on your online shop in marketplace?",
      "first_heading": "How to increase Page Views on your online shop in marketplace?"
    }
  },
  {
    "path": "blog_how-to-optimize-your-amazon-sponsored-products--ppc--keywords.html",
    "context": {
      "title": "How to Optimize Your Amazon Sponsored Products (PPC) Keywords",
      "first_heading": "How to Optimize Your Amazon Sponsored Products (PPC) Keywords"
    }
  },
  {
    "path": "blog_how-to-remove-negative-feedback-on-your-products-on-amazon-.html",
    "context": {
      "title": "How to Remove Negative Feedback On your Products on Amazon?",
      "first_heading": "How to Remove Negative Feedback On your Products on Amazon?"
    }
  },
  {
    "path": "blog_increase-your-conversions-to-increase-your-revenue.html",
    "context": {
      "title": "Increase Your Conversions To Increase Your Revenue",
      "first_heading": "Increase Your Conversions To Increase Your Revenue"
    }
  },
  {
    "path": "blog_what-is-amazon-buy-box--how-to-win-amazon-buy-box-.html",
    "context": {
      "title": "What is Amazon Buy box? How to win Amazon Buy box?",
      "first_heading": "What is Amazon Buy box? How to win Amazon Buy box?"
    }
  },
  {
    "path": "blog_what-to-do-when-you-receive-a-damaged-product-from-buyer-in-case-of-easy-ship-on-amazon--.html",
    "context": {
      "title": "What to do when you receive a damaged product from buyer in case of easy ship on Amazon?",
      "first_heading": "What to do when you receive a damaged product from buyer in case of easy ship on Amazon?"
    }
  },
  {
    "path": "css/0e222dfb63e9e8efe16d4082244ac3e1.css",
    "context": {
      "path": "css/0e222dfb63e9e8efe16d4082244ac3e1.css"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/65831fd6f1f49993e1646660d8747450.css",
    "context": {
      "path": "css/65831fd6f1f49993e1646660d8747450.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c280e70a6f4e43fa117c8e590b4022bc.css",
    "context": {
      "path": "css/c280e70a6f4e43fa117c8e590b4022bc.css"
    }
  },
  {
    "path": "css/eca01d6fc8d2d7aca2c856baa355437e.css",
    "context": {
      "path": "css/eca01d6fc8d2d7aca2c856baa355437e.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "digital-marketing-services.html",
    "context": {
      "title": "Best Digital Marketing Services in Jaipur | Online Marketing Services",
      "first_heading": "Reach us :7014511606Send Email"
    }
  },
  {
    "path": "imgs/044bb600c3c420a0881eb755486fbbf7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/045d3ae6f5a3dfcf1ffd2210e9de68a6.webp",
    "context": {
      "refs": [
        {
          "alt": "amazon account manager in jaipur, Amazon services in jaipur, ecommerce consultants in jaipur, ecomme",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/054382fc6547f21d7504d879fedca49b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0867b59d6eee5f17f1a579a8d0a9a066.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e11f39000b9373e92695924a60038a8.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/142ef992924dc47ec1d283b11ca09461.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18d6da84f5d7e7985c2aac657d0da089.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/256cefa1f28f0c3bba9874c3c18676cb.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/288723bf6968373e7c081df320875378.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e8fadc5aecda52d6a1d0241cdf60837.webp",
    "context": {
      "refs": [
        {
          "alt": "Amazon services, Amazon Global Services, Amazon india services, Amazon product listing, Amazon servi",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33732d848b63c9bacb3066374b6fee12.webp",
    "context": {
      "refs": [
        {
          "alt": "amazon service provider network",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ce3317850cb36c0c9fd0198e4ec24f3.webp",
    "context": {
      "refs": [
        {
          "alt": "Increase Traffic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/43dc718185d0c473d441789db92b8ff6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47ad269819b50b09e4d5c6dddd6f98b8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49e8e9ab00f996e246551baa9c852b94.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4dd028f6b48c9e197d71b6eebe895333.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        },
        {
          "alt": "Pay Per Click",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e8ba1a9b5f4085e84436f91cb23061f.webp",
    "context": {
      "refs": [
        {
          "alt": "Amazon Photo Shoot in jaipur, Amazon Seller Services, Amazon Business training, Online business serv",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/518ab078477d45231cba2aa42f8a247d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/534c08fad641df7a10e45baac36e7fb7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5390f88f74685df28df0da75f0cc64a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57f423ed527de5d796ced34ce9935bf1.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/606e7f276b04b38945c86d056961caec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6181324e135780b3c4bf8ea1e5d72515.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64dd022b003b5cf37ff76eee7eee23a9.webp",
    "context": {
      "refs": [
        {
          "alt": "Outside Insight of Your Business",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/663acf73f9b8464670697229f605ba1b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6c0a5b190265fc54bbcd2f350760ac65.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f80b8f261ee9e641070bd8de93cef1d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70b8fa24fda180bed92b8fc884575375.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/710f90b6d81f814fc1b755528a3e4ed6.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/745b32dbfceab652a006a7ab37176b7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7713b61412e33d3ac4b1d3e4d92dd491.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7fa69eb94991f7cc8d11c7c94ab89db7.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8866124f4ce6147ac12017226decf302.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92b54aa1dc2d5962481e3afd48badb6d.webp",
    "context": {
      "refs": [
        {
          "alt": "Amazon Online business in jaipur, Amazon Product Listing in jaipur, Amazon Cataloging service in jai",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/958123b25948a1bc1746bfbd34b6e012.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/975ca2a2ec7b75649adf2e4fee5efe69.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99f33e74163e1e9b7d3a6f175d8fac57.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a00019a5d67e0a73d0852bf22f8bd62b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a13a7b172120dd6981538ac322280a46.webp",
    "context": {
      "refs": [
        {
          "alt": "Amazon services, Amazon Global Services, Amazon india services, Amazon product listing, Amazon servi",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1d2d5fae6c76273673e0c7b0d05a5e5.webp",
    "context": {
      "refs": [
        {
          "alt": "Amazon Seller Training in jaipur, amazon training center in jaipur, Amazon business Training in jaip",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2924b85b2a6eb14f3080724cd55774f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a6dbc747dd1610cdea7bd1c3b0db4f0f.webp",
    "context": {
      "refs": [
        {
          "alt": "We understand what your site needs!",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab8f714d5439da9dfe9566f00b463687.webp",
    "context": {
      "refs": [
        {
          "alt": "Amazon Service in jaipur, Amazon global Services, Amazon seller services, Online business Services, ",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad5c7a39d516ba6afa47ee99ba8f917f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1739e6559daa622281819a81d72699c.webp",
    "context": {
      "refs": [
        {
          "alt": "amazon account manager in jaipur, amazon account management service in jaipur, amazon account handli",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8ddb3480ce7ceaf358a94ad2f2dff50.webp",
    "context": {
      "refs": [
        {
          "alt": "Assured Return on Investment",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd2ea84a0a424fa191e4e2053f5642bd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c13f6b1dbce57fd03fe907da5604969b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c680095c406c2dc65e6828eca298e745.webp",
    "context": {
      "refs": [
        {
          "alt": "On-Boarding Team of Experts",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbfddd9d05516f4516e37a78d9bd030f.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d04e84238adb993ae4b71f56b1867bad.webp",
    "context": {
      "refs": [
        {
          "alt": "amazon account management service in jaipur, amazon account manager, amazon account manager in jaipu",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0a4a8909cdc6638266157ebc45d234b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d27a8fe2d60017a12f8777dbdbbae8d9.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d50673b109c27f7d9f7c7978883564a7.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9df5f68f6c19b033c99a0277e5bbbba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1ae32c662880b4f9bcc2aed1e83f837.webp",
    "context": {
      "refs": [
        {
          "alt": "Lead Generation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8598efdf9fcecf8ec9055e02f616442.webp",
    "context": {
      "refs": [
        {
          "alt": "Social Media Marketing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e94d39d77242241abf7608590ede1f2a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eae7748f21202fcac26f786f245604a7.webp",
    "context": {
      "refs": [
        {
          "alt": "Brand Awareness",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/efeeffec65859bc36de1147b334ff025.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f063575bbe361f27cf7d27de68042fe3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f47c0a812b3fd4bfaab5ca5ca5ded9a9.webp",
    "context": {
      "refs": [
        {
          "alt": "amazon global selling services at revanth infotech jaipur, amazon international business services in",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f50521f18b934eea1ee48f6ca4b36aac.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8a171a598b3853121eed28866e00490.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd7e06cc65eba60ddf7c13f49d3091d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fdd881bc49c099ff66169ad372d35855.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Authorized Amazon Seller Service Provider Network in Jaipur Rajasthan India UAE",
      "first_heading": "REVANTH INFOTECH"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/5f3319a9548d4178ef43062afdfcffc7.js",
    "context": {
      "path": "js/5f3319a9548d4178ef43062afdfcffc7.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "product_AmazonStarterTraining.html",
    "context": {
      "title": "Amazon Seller Training In Jaipur",
      "first_heading": "Amazon Starter Training"
    }
  },
  {
    "path": "terms-Contditions.html",
    "context": {
      "title": "AUTHORISED AMAZON SERVICE PROVIDER",
      "first_heading": ""
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.