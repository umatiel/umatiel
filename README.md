async function run(title, url) {
      const keyword = [ 
            url 
      ] 
      //각 화 URL추출
      const result = await getUrl(keyword + "") 
      console.log(result) 

      //텍스트 추출
     const text = await getText(result) 

      //텍본 생성
      fs.writeFile('./textFile/' + title + '.txt', text, err => {
           if (err) {
               console.error(err) 
               return 
           }
           //file written successfully 
       }) 
}
// run("얀데레 아카데미의 회귀자", "https://novelpia.com/novel/32533")
