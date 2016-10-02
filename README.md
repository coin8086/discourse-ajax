# discourse-ajax
Discourse Ajax patch for CDN/server that doesn't support HTTP DELETE method

CDN is very important for Discourse since the latter has a lot of small images. However, some *smart* CDN who declares its easy usage by simply configurating some DNS settings and not invovling any code change *may* trap you for they don't support HTTP DELETE method. Aliyun CDN is just one of the example. 

That's too bad since Discourse doesn't work properly without DELETE. However, there's a good news that Ruby Rack has a feature called *method override*, which allows you to use POST for DELETE. This patch is just for this to work in Discourse. BTW, I suggested a feature for making such an option in Discourse admin panel but it's not been adopted. You may support me at https://meta.discourse.org/t/how-can-discourse-make-post-instead-of-delete-for-smart-cdn/43666
