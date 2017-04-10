var a = [].slice.call(document.querySelectorAll('#course li a')), html='', arr=[];
console.log(a);
a.forEach(function(item,index){
    //console.log(item);
    let href = item.getAttribute('href'), text = item.innerText;
    href = href.indexOf('..') >-1? href.replace('../',''): location.href.split('/')[4]+'/'+href;
    href = 'http://caibaojian.com/w3school/'+href;
//     console.log(href,text);

    html+= '* ['+text+']('+href+')\n';
})
console.log(html);
//document.body.innerText = html;
