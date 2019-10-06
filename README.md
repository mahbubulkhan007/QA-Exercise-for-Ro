# QA-Exercise-for-Ro
Test scenario for vaginal-dryness

@Test(priority = 1)
        public void Vaginal_Dryness() throws InterruptedException {
       // Acceptance criteria: User should be able to enter Email address
            String Email = "Mahbubul.y@gmail.com";
            driver.findElement(By.xpath("//*[@id=\"app\"]/div[2]/div[1]/div/div/div/div/div[2]/div/form/div[1]/div[1]")).click();
            Thread.sleep(3000);

           List<WebElement> output = driver.findElements(By.xpath("//*[@id=\'temporaryEmail\']"));
           int count = output.size();
           System.out.println("Total elenent is: " + output.size());
           for (int i=0;i<count;i++)
           {
               int x = output.get(i).getLocation().getX();
               if (x!=0);
               {
                   output.get(i).sendKeys("Mahbubul.y@gmail.com");
                   break;
               }

           }
            driver.findElement(By.xpath("//*[@id=\'temporaryEmail\']")).sendKeys("value", "Mahbubul.y@gmail.com");

                driver.findElement(By.xpath(".//*[@id=\'temporaryEmail\']")).sendKeys("Mahbubul.y@gmail.com");
