<a id="link" href="#" download></a>

<div>种子文件下载完毕，当前页面可以关掉了</div>

<script>
      console.log('download file')
      const a = document.querySelector('#link');
      const file = window.location.href.match(/(?<=file=)(.*)/)[0];
      console.log({ file });
      if (file) {
        a.setAttribute('href', file);
        a.click();
      }
</script>
